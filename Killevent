package Piratewars;
 
import java.util.ArrayList;

import org.bukkit.ChatColor;
import org.bukkit.Material;
import org.bukkit.Sound;
import org.bukkit.entity.LivingEntity;
import org.bukkit.entity.Player;
import org.bukkit.event.EventHandler;
import org.bukkit.event.Listener;
import org.bukkit.event.entity.EntityDeathEvent;
import org.bukkit.inventory.ItemStack;
import org.bukkit.inventory.meta.ItemMeta;
 
public class Killevent implements Listener {
 
    @EventHandler
   public void onDeath(EntityDeathEvent e) {
    	
    	ItemStack coin = new ItemStack(Material.GOLD_NUGGET, 3);
		ItemMeta coinMeta = coin.getItemMeta();
		
		coinMeta.setDisplayName("" + ChatColor.GOLD + ChatColor.BOLD + "COIN");
		ArrayList<String> coinlore = new ArrayList<String>();
		coinlore.add("§eCoins are used to buy gadgets in the PirateWars Shop");
		coinMeta.setLore(coinlore);
		coin.setItemMeta(coinMeta);
    	
     LivingEntity p = e.getEntity();
     if(p.getKiller() instanceof Player) {
        Player d = p.getKiller();
{
      d.playSound(p.getKiller().getLocation(), Sound.ENDERDRAGON_GROWL, 5, 5);
    d.getInventory().addItem(coin);
       }
     }
    }
}
