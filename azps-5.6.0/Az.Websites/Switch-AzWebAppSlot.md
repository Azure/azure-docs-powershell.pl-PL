---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 7cb74e6eec27df299206ee62264588a37dee3a2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010993"
---
# <span data-ttu-id="49869-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="49869-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="49869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49869-102">SYNOPSIS</span></span>
<span data-ttu-id="49869-103">Zamiana dwóch miejsc za pomocą aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="49869-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="49869-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49869-104">SYNTAX</span></span>

### <span data-ttu-id="49869-105">S1</span><span class="sxs-lookup"><span data-stu-id="49869-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49869-106">S2</span><span class="sxs-lookup"><span data-stu-id="49869-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49869-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="49869-107">DESCRIPTION</span></span>
<span data-ttu-id="49869-108">Przełącznik **AzWebAppSlot** przełącza dwa gniazda skojarzone z aplikacją Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="49869-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="49869-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49869-109">EXAMPLES</span></span>

### <span data-ttu-id="49869-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49869-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="49869-111">To polecenie przełączy slot "sourceslot" na "destinationslot" w aplikacji Web App ContosoWebApp skojarzonej z grupą zasobów Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="49869-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="49869-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49869-112">PARAMETERS</span></span>

### <span data-ttu-id="49869-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49869-113">-DefaultProfile</span></span>
<span data-ttu-id="49869-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49869-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49869-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="49869-115">-DestinationSlotName</span></span>
<span data-ttu-id="49869-116">Nazwa miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="49869-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="49869-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49869-117">-Name</span></span>
<span data-ttu-id="49869-118">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="49869-118">WebApp Name</span></span>

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

### <span data-ttu-id="49869-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="49869-119">-PreserveVnet</span></span>
<span data-ttu-id="49869-120">Zachowaj wartość logiczną Vnet</span><span class="sxs-lookup"><span data-stu-id="49869-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="49869-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49869-121">-ResourceGroupName</span></span>
<span data-ttu-id="49869-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="49869-122">Resource Group Name</span></span>

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

### <span data-ttu-id="49869-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="49869-123">-SourceSlotName</span></span>
<span data-ttu-id="49869-124">Nazwa gniazda źródłowego</span><span class="sxs-lookup"><span data-stu-id="49869-124">Source Slot Name</span></span>

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

### <span data-ttu-id="49869-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="49869-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="49869-126">Zamiana z akcją podglądu</span><span class="sxs-lookup"><span data-stu-id="49869-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="49869-127">- WebApp</span><span class="sxs-lookup"><span data-stu-id="49869-127">-WebApp</span></span>
<span data-ttu-id="49869-128">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="49869-128">WebApp Object</span></span>

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

### <span data-ttu-id="49869-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49869-129">-Confirm</span></span>
<span data-ttu-id="49869-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49869-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49869-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49869-131">-WhatIf</span></span>
<span data-ttu-id="49869-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49869-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49869-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49869-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49869-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49869-134">CommonParameters</span></span>
<span data-ttu-id="49869-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49869-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49869-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49869-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49869-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49869-137">INPUTS</span></span>

### <span data-ttu-id="49869-138">System.String</span><span class="sxs-lookup"><span data-stu-id="49869-138">System.String</span></span>

### <span data-ttu-id="49869-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="49869-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="49869-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49869-140">OUTPUTS</span></span>

### <span data-ttu-id="49869-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="49869-141">System.Void</span></span>

## <span data-ttu-id="49869-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49869-142">NOTES</span></span>

## <span data-ttu-id="49869-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49869-143">RELATED LINKS</span></span>
