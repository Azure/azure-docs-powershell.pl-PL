---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: 9522fe6925ac266ff87f3ba6b3540980d91c160f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719605"
---
# <span data-ttu-id="517cb-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="517cb-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="517cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="517cb-102">SYNOPSIS</span></span>
<span data-ttu-id="517cb-103">Wymiana dwóch gniazd za pomocą aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="517cb-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="517cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="517cb-104">SYNTAX</span></span>

### <span data-ttu-id="517cb-105">S1</span><span class="sxs-lookup"><span data-stu-id="517cb-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517cb-106">S2</span><span class="sxs-lookup"><span data-stu-id="517cb-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517cb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="517cb-107">DESCRIPTION</span></span>
<span data-ttu-id="517cb-108">**Przełącznik Switch-AzureRmWebAppSlot** przełącza dwa gniazda skojarzone z aplikacją Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="517cb-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="517cb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="517cb-109">EXAMPLES</span></span>

### <span data-ttu-id="517cb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="517cb-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="517cb-111">To polecenie spowoduje przełączenie gniazda "sourceslot" z "destinationslot" dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="517cb-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="517cb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="517cb-112">PARAMETERS</span></span>

### <span data-ttu-id="517cb-113">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="517cb-113">-DestinationSlotName</span></span>
<span data-ttu-id="517cb-114">Nazwa miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="517cb-114">Destination Slot Name</span></span>

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

### <span data-ttu-id="517cb-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="517cb-115">-Name</span></span>
<span data-ttu-id="517cb-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="517cb-116">WebApp Name</span></span>

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

### <span data-ttu-id="517cb-117">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="517cb-117">-PreserveVnet</span></span>
<span data-ttu-id="517cb-118">Zachowaj wartość logiczną VNET</span><span class="sxs-lookup"><span data-stu-id="517cb-118">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="517cb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="517cb-119">-ResourceGroupName</span></span>
<span data-ttu-id="517cb-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="517cb-120">Resource Group Name</span></span>

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

### <span data-ttu-id="517cb-121">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="517cb-121">-SourceSlotName</span></span>
<span data-ttu-id="517cb-122">Nazwa miejsca źródłowego</span><span class="sxs-lookup"><span data-stu-id="517cb-122">Source Slot Name</span></span>

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

### <span data-ttu-id="517cb-123">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="517cb-123">-SwapWithPreviewAction</span></span>
<span data-ttu-id="517cb-124">Zamień na akcję w wersji Preview</span><span class="sxs-lookup"><span data-stu-id="517cb-124">Swap With Preview Action</span></span>

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

### <span data-ttu-id="517cb-125">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="517cb-125">-WebApp</span></span>
<span data-ttu-id="517cb-126">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="517cb-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="517cb-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="517cb-127">-Confirm</span></span>
<span data-ttu-id="517cb-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="517cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517cb-129">-WhatIf</span></span>
<span data-ttu-id="517cb-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517cb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="517cb-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="517cb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="517cb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517cb-132">-DefaultProfile</span></span>
<span data-ttu-id="517cb-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="517cb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="517cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517cb-134">CommonParameters</span></span>
<span data-ttu-id="517cb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517cb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517cb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517cb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="517cb-137">INPUTS</span></span>

### <span data-ttu-id="517cb-138">Klienta</span><span class="sxs-lookup"><span data-stu-id="517cb-138">Site</span></span>
<span data-ttu-id="517cb-139">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="517cb-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="517cb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="517cb-140">OUTPUTS</span></span>

## <span data-ttu-id="517cb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="517cb-141">NOTES</span></span>

## <span data-ttu-id="517cb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="517cb-142">RELATED LINKS</span></span>

