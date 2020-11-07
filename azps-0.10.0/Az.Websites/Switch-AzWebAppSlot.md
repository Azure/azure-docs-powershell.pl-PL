---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891798"
---
# <span data-ttu-id="a360f-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a360f-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="a360f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a360f-102">SYNOPSIS</span></span>
<span data-ttu-id="a360f-103">Wymiana dwóch gniazd za pomocą aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="a360f-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="a360f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a360f-104">SYNTAX</span></span>

### <span data-ttu-id="a360f-105">S1</span><span class="sxs-lookup"><span data-stu-id="a360f-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a360f-106">S2</span><span class="sxs-lookup"><span data-stu-id="a360f-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a360f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a360f-107">DESCRIPTION</span></span>
<span data-ttu-id="a360f-108">**Przełącznik Switch-AzWebAppSlot** przełącza dwa gniazda skojarzone z aplikacją Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a360f-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="a360f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a360f-109">EXAMPLES</span></span>

### <span data-ttu-id="a360f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a360f-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a360f-111">To polecenie spowoduje przełączenie gniazda "sourceslot" na "destinationslot" dla aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="a360f-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a360f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a360f-112">PARAMETERS</span></span>

### <span data-ttu-id="a360f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a360f-113">-DefaultProfile</span></span>
<span data-ttu-id="a360f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a360f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360f-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="a360f-115">-DestinationSlotName</span></span>
<span data-ttu-id="a360f-116">Nazwa miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="a360f-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a360f-117">-Name</span></span>
<span data-ttu-id="a360f-118">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="a360f-118">WebApp Name</span></span>

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

### <span data-ttu-id="a360f-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="a360f-119">-PreserveVnet</span></span>
<span data-ttu-id="a360f-120">Zachowaj wartość logiczną VNET</span><span class="sxs-lookup"><span data-stu-id="a360f-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a360f-121">-ResourceGroupName</span></span>
<span data-ttu-id="a360f-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a360f-122">Resource Group Name</span></span>

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

### <span data-ttu-id="a360f-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="a360f-123">-SourceSlotName</span></span>
<span data-ttu-id="a360f-124">Nazwa miejsca źródłowego</span><span class="sxs-lookup"><span data-stu-id="a360f-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360f-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="a360f-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="a360f-126">Zamień na akcję w wersji Preview</span><span class="sxs-lookup"><span data-stu-id="a360f-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a360f-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a360f-127">-WebApp</span></span>
<span data-ttu-id="a360f-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="a360f-128">WebApp Object</span></span>

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

### <span data-ttu-id="a360f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a360f-129">-Confirm</span></span>
<span data-ttu-id="a360f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a360f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a360f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a360f-131">-WhatIf</span></span>
<span data-ttu-id="a360f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a360f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a360f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a360f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a360f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a360f-134">CommonParameters</span></span>
<span data-ttu-id="a360f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a360f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a360f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a360f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a360f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a360f-137">INPUTS</span></span>

### <span data-ttu-id="a360f-138">Klienta</span><span class="sxs-lookup"><span data-stu-id="a360f-138">Site</span></span>
<span data-ttu-id="a360f-139">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="a360f-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a360f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a360f-140">OUTPUTS</span></span>

## <span data-ttu-id="a360f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a360f-141">NOTES</span></span>

## <span data-ttu-id="a360f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a360f-142">RELATED LINKS</span></span>

