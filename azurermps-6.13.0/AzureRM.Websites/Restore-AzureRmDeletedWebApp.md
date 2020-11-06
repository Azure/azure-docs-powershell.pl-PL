---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546299"
---
# Restore-AzureRmDeletedWebApp

## STRESZCZENIe
Przywraca usuniętą aplikację internetową do nowej lub istniejącej aplikacji sieci Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### FromDeletedResourceName
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedApp
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Restore-AzureRmDeletedWebApp** powoduje przywrócenie usuniętej aplikacji sieci Web. Aplikacja sieci Web określona przez TargetResourceGroupName, TargetName i TargetSlot zostanie zastąpiona zawartością i ustawieniami usuniętej aplikacji sieci Web. Jeśli parametry docelowe nie zostaną określone, zostaną automatycznie wypełnione w grupie zasobów, nazwie i gnieździe usuniętej aplikacji sieci Web. Jeśli docelowa aplikacja sieci Web nie istnieje, zostanie automatycznie utworzona w planie usługi App Service określonym przez TargetAppServicePlanName. Parametr przełącznika RestoreContentOnly można użyć w celu przywrócenia tylko plików usuniętej aplikacji bez ustawień aplikacji.

## Przykłady

### Przykład 1
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

Przywraca usuniętą aplikację o nazwie ContosoApp należącą do grupy zasobów Default — Web-Zachodnia. W planie usługi App Service o nazwie ContosoPlan zostanie utworzona nowa aplikacja z tą samą nazwą i grupą, a pliki i ustawienia aplikacji usunięte zostaną przywrócone.

### Przykład 2
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

Przywraca miejsce przemieszczania usuniętej aplikacji o nazwie ContosoApp należącej do grupy zasobów Default-Web-Zachodnia. Aplikacja sieci Web o nazwie ContosoRestore należąca do grupy zasobów domyślne — sieć Web-wschód zostanie zastąpiona. Usunięte ustawienia aplikacji sieci Web nie zostaną przywrócone.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wykonaj przywracanie bez monitowania o potwierdzenie.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Usunięta aplikacja Azure Web App.

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa usuniętej aplikacji sieci Web platformy Azure.

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów usuniętej aplikacji sieci Web platformy Azure.

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreContentOnly
Przywróć pliki aplikacji sieci Web, ale nie przywracaj ustawień.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Usunięte gniazdo aplikacji sieci Web platformy Azure.

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAppServicePlanName
Plan usługi App Service dla nowej aplikacji sieci Web platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetName
Nazwa nowej aplikacji sieci Web platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName
Grupa zasobów zawierająca nową aplikację sieci Web platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetSlot
Nazwa nowego miejsca w aplikacji Azure Web App.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.
Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp

## WYSYŁA

### Microsoft. Azure. Commands. webapps. modele. PSSite

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmDeletedWebApp](./Get-AzureRmDeletedWebApp.md)
