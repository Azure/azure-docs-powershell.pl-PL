---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546331"
---
# <span data-ttu-id="c2763-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c2763-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2763-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2763-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2763-103">SYNTAX</span></span>

### <span data-ttu-id="c2763-104">S1</span><span class="sxs-lookup"><span data-stu-id="c2763-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2763-105">S2</span><span class="sxs-lookup"><span data-stu-id="c2763-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2763-106">Opis</span><span class="sxs-lookup"><span data-stu-id="c2763-106">DESCRIPTION</span></span>
<span data-ttu-id="c2763-107">Polecenie cmdlet **Remove-AzureRmWebAppSlot** usuwa miejsce w usłudze Azure Web App, pod warunkiem, że grupa zasobów i nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c2763-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="c2763-108">To polecenie cmdlet domyślnie usuwa także wszystkie gniazda i metryki.</span><span class="sxs-lookup"><span data-stu-id="c2763-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="c2763-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2763-109">EXAMPLES</span></span>

### <span data-ttu-id="c2763-110">Przykład 1. Usuń miejsce aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="c2763-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="c2763-111">To polecenie powoduje usunięcie gniazda o nazwie Slot001 skojarzonego z aplikacją sieci Web ContosoSite należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c2763-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c2763-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2763-112">PARAMETERS</span></span>

### <span data-ttu-id="c2763-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2763-113">-AsJob</span></span>
<span data-ttu-id="c2763-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c2763-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2763-115">-DefaultProfile</span></span>
<span data-ttu-id="c2763-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2763-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c2763-117">-Force</span></span>
<span data-ttu-id="c2763-118">Wymuszone usuwanie opcji</span><span class="sxs-lookup"><span data-stu-id="c2763-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2763-119">-Name</span></span>
<span data-ttu-id="c2763-120">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c2763-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2763-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2763-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c2763-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="c2763-123">-Slot</span></span>
<span data-ttu-id="c2763-124">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="c2763-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c2763-125">-WebApp</span></span>
<span data-ttu-id="c2763-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c2763-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2763-127">-Confirm</span></span>
<span data-ttu-id="c2763-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2763-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2763-129">-WhatIf</span></span>
<span data-ttu-id="c2763-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2763-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2763-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2763-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2763-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2763-132">CommonParameters</span></span>
<span data-ttu-id="c2763-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2763-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2763-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2763-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2763-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2763-135">INPUTS</span></span>

### <span data-ttu-id="c2763-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2763-136">System.String</span></span>

### <span data-ttu-id="c2763-137">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="c2763-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c2763-138">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c2763-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c2763-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2763-139">OUTPUTS</span></span>

### <span data-ttu-id="c2763-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c2763-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c2763-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2763-141">NOTES</span></span>

## <span data-ttu-id="c2763-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2763-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2763-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2763-144">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2763-145">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2763-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2763-147">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2763-148">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c2763-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c2763-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c2763-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
