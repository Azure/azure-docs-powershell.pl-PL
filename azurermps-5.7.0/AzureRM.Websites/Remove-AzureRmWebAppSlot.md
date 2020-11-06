---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551467"
---
# <span data-ttu-id="8fcf0-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="8fcf0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fcf0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fcf0-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fcf0-103">SYNTAX</span></span>

### <span data-ttu-id="8fcf0-104">S1</span><span class="sxs-lookup"><span data-stu-id="8fcf0-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fcf0-105">S2</span><span class="sxs-lookup"><span data-stu-id="8fcf0-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fcf0-106">Opis</span><span class="sxs-lookup"><span data-stu-id="8fcf0-106">DESCRIPTION</span></span>
<span data-ttu-id="8fcf0-107">Polecenie cmdlet **Remove-AzureRmWebAppSlot** usuwa miejsce w usłudze Azure Web App, pod warunkiem, że grupa zasobów i nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="8fcf0-108">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="8fcf0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fcf0-109">EXAMPLES</span></span>

### <span data-ttu-id="8fcf0-110">Przykład 1. Usuń miejsce aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="8fcf0-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="8fcf0-111">To polecenie powoduje usunięcie gniazda o nazwie Slot001 skojarzonego z aplikacją sieci Web ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8fcf0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fcf0-112">PARAMETERS</span></span>

### <span data-ttu-id="8fcf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fcf0-113">-DefaultProfile</span></span>
<span data-ttu-id="8fcf0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fcf0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8fcf0-115">-Force</span></span>
<span data-ttu-id="8fcf0-116">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="8fcf0-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="8fcf0-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8fcf0-117">-Name</span></span>
<span data-ttu-id="8fcf0-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="8fcf0-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fcf0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fcf0-119">-ResourceGroupName</span></span>
<span data-ttu-id="8fcf0-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8fcf0-120">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fcf0-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-121">-Slot</span></span>
<span data-ttu-id="8fcf0-122">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="8fcf0-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fcf0-123">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="8fcf0-123">-WebApp</span></span>
<span data-ttu-id="8fcf0-124">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="8fcf0-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fcf0-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8fcf0-125">-Confirm</span></span>
<span data-ttu-id="8fcf0-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fcf0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fcf0-127">-WhatIf</span></span>
<span data-ttu-id="8fcf0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fcf0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="8fcf0-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fcf0-130">-AsJob</span></span>
<span data-ttu-id="8fcf0-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8fcf0-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fcf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fcf0-132">CommonParameters</span></span>
<span data-ttu-id="8fcf0-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fcf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fcf0-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fcf0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fcf0-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fcf0-135">INPUTS</span></span>

### <span data-ttu-id="8fcf0-136">Klienta</span><span class="sxs-lookup"><span data-stu-id="8fcf0-136">Site</span></span>
<span data-ttu-id="8fcf0-137">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="8fcf0-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8fcf0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fcf0-138">OUTPUTS</span></span>

### <span data-ttu-id="8fcf0-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8fcf0-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8fcf0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fcf0-140">NOTES</span></span>

## <span data-ttu-id="8fcf0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fcf0-141">RELATED LINKS</span></span>

[<span data-ttu-id="8fcf0-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="8fcf0-143">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="8fcf0-144">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="8fcf0-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="8fcf0-146">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="8fcf0-147">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8fcf0-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="8fcf0-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8fcf0-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
