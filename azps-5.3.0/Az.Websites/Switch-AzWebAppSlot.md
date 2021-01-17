---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491393"
---
# <span data-ttu-id="52bc6-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="52bc6-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="52bc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="52bc6-103">Wymiana dwóch gniazd za pomocą aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="52bc6-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="52bc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52bc6-104">SYNTAX</span></span>

### <span data-ttu-id="52bc6-105">S1</span><span class="sxs-lookup"><span data-stu-id="52bc6-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52bc6-106">S2</span><span class="sxs-lookup"><span data-stu-id="52bc6-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52bc6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="52bc6-107">DESCRIPTION</span></span>
<span data-ttu-id="52bc6-108">**Przełącznik Switch-AzWebAppSlot** przełącza dwa gniazda skojarzone z aplikacją Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="52bc6-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="52bc6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52bc6-109">EXAMPLES</span></span>

### <span data-ttu-id="52bc6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52bc6-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="52bc6-111">To polecenie spowoduje przełączenie gniazda "sourceslot" na "destinationslot" aplikacji sieci Web ContosoWebApp skojarzonej z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="52bc6-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="52bc6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52bc6-112">PARAMETERS</span></span>

### <span data-ttu-id="52bc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bc6-113">-DefaultProfile</span></span>
<span data-ttu-id="52bc6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc6-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="52bc6-115">-DestinationSlotName</span></span>
<span data-ttu-id="52bc6-116">Nazwa miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="52bc6-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52bc6-117">-Name</span></span>
<span data-ttu-id="52bc6-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="52bc6-118">WebApp Name</span></span>

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

### <span data-ttu-id="52bc6-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="52bc6-119">-PreserveVnet</span></span>
<span data-ttu-id="52bc6-120">Zachowaj wartość logiczną VNET</span><span class="sxs-lookup"><span data-stu-id="52bc6-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52bc6-121">-ResourceGroupName</span></span>
<span data-ttu-id="52bc6-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="52bc6-122">Resource Group Name</span></span>

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

### <span data-ttu-id="52bc6-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="52bc6-123">-SourceSlotName</span></span>
<span data-ttu-id="52bc6-124">Nazwa miejsca źródłowego</span><span class="sxs-lookup"><span data-stu-id="52bc6-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc6-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="52bc6-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="52bc6-126">Zamień na akcję w wersji Preview</span><span class="sxs-lookup"><span data-stu-id="52bc6-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc6-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="52bc6-127">-WebApp</span></span>
<span data-ttu-id="52bc6-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="52bc6-128">WebApp Object</span></span>

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

### <span data-ttu-id="52bc6-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52bc6-129">-Confirm</span></span>
<span data-ttu-id="52bc6-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bc6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52bc6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52bc6-131">-WhatIf</span></span>
<span data-ttu-id="52bc6-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bc6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52bc6-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52bc6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52bc6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bc6-134">CommonParameters</span></span>
<span data-ttu-id="52bc6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52bc6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bc6-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52bc6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bc6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52bc6-137">INPUTS</span></span>

### <span data-ttu-id="52bc6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="52bc6-138">System.String</span></span>

### <span data-ttu-id="52bc6-139">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="52bc6-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="52bc6-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52bc6-140">OUTPUTS</span></span>

### <span data-ttu-id="52bc6-141">System. void</span><span class="sxs-lookup"><span data-stu-id="52bc6-141">System.Void</span></span>

## <span data-ttu-id="52bc6-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52bc6-142">NOTES</span></span>

## <span data-ttu-id="52bc6-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52bc6-143">RELATED LINKS</span></span>
