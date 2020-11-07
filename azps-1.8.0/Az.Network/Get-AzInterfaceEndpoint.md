---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709529"
---
# <span data-ttu-id="79766-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="79766-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="79766-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79766-102">SYNOPSIS</span></span>
<span data-ttu-id="79766-103">Polecenie cmdlet Get-AzInterfaceEndpoint Pobiera punkt końcowy interfejsu.</span><span class="sxs-lookup"><span data-stu-id="79766-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="79766-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79766-104">SYNTAX</span></span>

### <span data-ttu-id="79766-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79766-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79766-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79766-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79766-107">Opis</span><span class="sxs-lookup"><span data-stu-id="79766-107">DESCRIPTION</span></span>
<span data-ttu-id="79766-108">Polecenie cmdlet **Get-AzInterfaceEndpoint** Pobiera punkt końcowy interfejsu.</span><span class="sxs-lookup"><span data-stu-id="79766-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="79766-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79766-109">EXAMPLES</span></span>

### <span data-ttu-id="79766-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79766-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="79766-111">To polecenie uzyskuje punkt końcowy o nazwie InterfaceEndpoint1 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="79766-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="79766-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="79766-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="79766-113">To polecenie uzyskuje punkt końcowy interfejsu z identyfikatorem zasobu resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 i zapisuje go w zmiennej $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="79766-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="79766-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="79766-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="79766-115">To polecenie uzyskuje punkty końcowe interfejsu rozpoczynające się od "InterfaceEndpoint"</span><span class="sxs-lookup"><span data-stu-id="79766-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="79766-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79766-116">PARAMETERS</span></span>

### <span data-ttu-id="79766-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79766-117">-DefaultProfile</span></span>
<span data-ttu-id="79766-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79766-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79766-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79766-119">-Name</span></span>
<span data-ttu-id="79766-120">Nazwa punktu końcowego interfejsu</span><span class="sxs-lookup"><span data-stu-id="79766-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="79766-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79766-121">-ResourceGroupName</span></span>
<span data-ttu-id="79766-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79766-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="79766-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79766-123">-ResourceId</span></span>
<span data-ttu-id="79766-124">Identyfikator punktu końcowego interfejsu.</span><span class="sxs-lookup"><span data-stu-id="79766-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79766-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79766-125">-Confirm</span></span>
<span data-ttu-id="79766-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79766-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79766-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79766-127">-WhatIf</span></span>
<span data-ttu-id="79766-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79766-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79766-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79766-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79766-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79766-130">CommonParameters</span></span>
<span data-ttu-id="79766-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79766-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79766-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79766-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79766-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79766-133">INPUTS</span></span>

### <span data-ttu-id="79766-134">System. String</span><span class="sxs-lookup"><span data-stu-id="79766-134">System.String</span></span>

## <span data-ttu-id="79766-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79766-135">OUTPUTS</span></span>

### <span data-ttu-id="79766-136">Microsoft. Azure. Commands. Network. models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="79766-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="79766-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79766-137">NOTES</span></span>

## <span data-ttu-id="79766-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79766-138">RELATED LINKS</span></span>
