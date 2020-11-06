---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545108"
---
# <span data-ttu-id="f4049-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4049-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="f4049-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4049-102">SYNOPSIS</span></span>
<span data-ttu-id="f4049-103">Polecenie cmdlet Get-AzureRmInterfaceEndpoint Pobiera punkt końcowy interfejsu.</span><span class="sxs-lookup"><span data-stu-id="f4049-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4049-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4049-104">SYNTAX</span></span>

### <span data-ttu-id="f4049-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4049-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4049-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4049-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4049-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4049-107">DESCRIPTION</span></span>
<span data-ttu-id="f4049-108">Polecenie cmdlet **Get-AzureRmInterfaceEndpoint** Pobiera punkt końcowy interfejsu.</span><span class="sxs-lookup"><span data-stu-id="f4049-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="f4049-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4049-109">EXAMPLES</span></span>

### <span data-ttu-id="f4049-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f4049-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f4049-111">To polecenie uzyskuje punkt końcowy o nazwie InterfaceEndpoint1 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="f4049-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="f4049-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f4049-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="f4049-113">To polecenie uzyskuje punkt końcowy interfejsu z identyfikatorem zasobu resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 i zapisuje go w zmiennej $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="f4049-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="f4049-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4049-114">PARAMETERS</span></span>

### <span data-ttu-id="f4049-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4049-115">-DefaultProfile</span></span>
<span data-ttu-id="f4049-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4049-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4049-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4049-117">-Name</span></span>
<span data-ttu-id="f4049-118">Nazwa punktu końcowego interfejsu</span><span class="sxs-lookup"><span data-stu-id="f4049-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4049-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4049-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4049-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4049-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4049-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4049-121">-ResourceId</span></span>
<span data-ttu-id="f4049-122">{{Opis ResourceId (wypełnienie)}}</span><span class="sxs-lookup"><span data-stu-id="f4049-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4049-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4049-123">-Confirm</span></span>
<span data-ttu-id="f4049-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4049-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4049-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4049-125">-WhatIf</span></span>
<span data-ttu-id="f4049-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4049-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4049-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4049-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4049-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4049-128">CommonParameters</span></span>
<span data-ttu-id="f4049-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4049-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f4049-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4049-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4049-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4049-131">INPUTS</span></span>

### <span data-ttu-id="f4049-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4049-132">System.String</span></span>


## <span data-ttu-id="f4049-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4049-133">OUTPUTS</span></span>

### <span data-ttu-id="f4049-134">Microsoft. Azure. Commands. Network. models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4049-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="f4049-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4049-135">NOTES</span></span>

## <span data-ttu-id="f4049-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4049-136">RELATED LINKS</span></span>
