---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993546"
---
# <span data-ttu-id="00975-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="00975-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="00975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00975-102">SYNOPSIS</span></span>
<span data-ttu-id="00975-103">Usuwa grupę strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="00975-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="00975-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00975-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00975-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="00975-105">DESCRIPTION</span></span>
<span data-ttu-id="00975-106">Polecenie **cmdlet Remove-AzPrivateDnsZoneGroup** usuwa grupę strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="00975-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="00975-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00975-107">EXAMPLES</span></span>

### <span data-ttu-id="00975-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00975-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="00975-109">Powyższy przykład usuwa grupę strefy DNS o nazwie dnsgroup1 z punktu końcowego test-pr-endpoint.</span><span class="sxs-lookup"><span data-stu-id="00975-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="00975-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00975-110">PARAMETERS</span></span>

### <span data-ttu-id="00975-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="00975-111">-AsJob</span></span>
<span data-ttu-id="00975-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="00975-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00975-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00975-113">-DefaultProfile</span></span>
<span data-ttu-id="00975-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00975-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00975-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="00975-115">-Force</span></span>
<span data-ttu-id="00975-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="00975-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="00975-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="00975-117">-Name</span></span>
<span data-ttu-id="00975-118">Nazwa prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="00975-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00975-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00975-119">-PassThru</span></span>
<span data-ttu-id="00975-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="00975-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="00975-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="00975-121">-PrivateEndpointName</span></span>
<span data-ttu-id="00975-122">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="00975-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00975-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00975-123">-ResourceGroupName</span></span>
<span data-ttu-id="00975-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="00975-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00975-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00975-125">-Confirm</span></span>
<span data-ttu-id="00975-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00975-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00975-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00975-127">-WhatIf</span></span>
<span data-ttu-id="00975-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00975-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00975-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="00975-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00975-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00975-130">CommonParameters</span></span>
<span data-ttu-id="00975-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00975-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00975-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00975-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00975-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00975-133">INPUTS</span></span>

### <span data-ttu-id="00975-134">System.String</span><span class="sxs-lookup"><span data-stu-id="00975-134">System.String</span></span>

## <span data-ttu-id="00975-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00975-135">OUTPUTS</span></span>

### <span data-ttu-id="00975-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00975-136">System.Boolean</span></span>

## <span data-ttu-id="00975-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00975-137">NOTES</span></span>

## <span data-ttu-id="00975-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00975-138">RELATED LINKS</span></span>
