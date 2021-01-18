---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504465"
---
# <span data-ttu-id="6dd64-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="6dd64-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="6dd64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dd64-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd64-103">Usuwa grupę stref DNS.</span><span class="sxs-lookup"><span data-stu-id="6dd64-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="6dd64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dd64-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd64-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6dd64-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd64-106">Polecenie cmdlet **Remove-AzPrivateDnsZoneGroup** usuwa grupę stref DNS.</span><span class="sxs-lookup"><span data-stu-id="6dd64-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="6dd64-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dd64-107">EXAMPLES</span></span>

### <span data-ttu-id="6dd64-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6dd64-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="6dd64-109">W powyższym przykładzie usunięto grupowe nazwy stref DNS o nazwie dnsgroup1 z punktu końcowego test-PR-Endpoint.</span><span class="sxs-lookup"><span data-stu-id="6dd64-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="6dd64-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dd64-110">PARAMETERS</span></span>

### <span data-ttu-id="6dd64-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dd64-111">-AsJob</span></span>
<span data-ttu-id="6dd64-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6dd64-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6dd64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd64-113">-DefaultProfile</span></span>
<span data-ttu-id="6dd64-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd64-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dd64-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6dd64-115">-Force</span></span>
<span data-ttu-id="6dd64-116">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="6dd64-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="6dd64-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dd64-117">-Name</span></span>
<span data-ttu-id="6dd64-118">Nazwa grupy prywatna strefa DNS.</span><span class="sxs-lookup"><span data-stu-id="6dd64-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="6dd64-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dd64-119">-PassThru</span></span>
<span data-ttu-id="6dd64-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6dd64-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6dd64-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="6dd64-121">-PrivateEndpointName</span></span>
<span data-ttu-id="6dd64-122">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6dd64-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="6dd64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd64-123">-ResourceGroupName</span></span>
<span data-ttu-id="6dd64-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6dd64-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6dd64-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6dd64-125">-Confirm</span></span>
<span data-ttu-id="6dd64-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd64-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd64-127">-WhatIf</span></span>
<span data-ttu-id="6dd64-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd64-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd64-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6dd64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd64-130">CommonParameters</span></span>
<span data-ttu-id="6dd64-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd64-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dd64-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd64-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dd64-133">INPUTS</span></span>

### <span data-ttu-id="6dd64-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6dd64-134">System.String</span></span>

## <span data-ttu-id="6dd64-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dd64-135">OUTPUTS</span></span>

### <span data-ttu-id="6dd64-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dd64-136">System.Boolean</span></span>

## <span data-ttu-id="6dd64-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dd64-137">NOTES</span></span>

## <span data-ttu-id="6dd64-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dd64-138">RELATED LINKS</span></span>
