---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500229"
---
# <span data-ttu-id="9d4a3-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9d4a3-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="9d4a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4a3-103">Usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-103">Removes a network security group.</span></span>

## <span data-ttu-id="9d4a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d4a3-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d4a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="9d4a3-106">Polecenie cmdlet **Remove-AzNetworkSecurityGroup** usuwa grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="9d4a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="9d4a3-108">Przykład 1. Usuń grupę zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="9d4a3-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="9d4a3-109">To polecenie usuwa grupę zabezpieczeń o nazwie NSG-FrontEnd w grupie zasobów o nazwie TestRG.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="9d4a3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d4a3-110">PARAMETERS</span></span>

### <span data-ttu-id="9d4a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d4a3-111">-AsJob</span></span>
<span data-ttu-id="9d4a3-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9d4a3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d4a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4a3-113">-DefaultProfile</span></span>
<span data-ttu-id="9d4a3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d4a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9d4a3-115">-Force</span></span>
<span data-ttu-id="9d4a3-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d4a3-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d4a3-117">-Name</span></span>
<span data-ttu-id="9d4a3-118">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d4a3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d4a3-119">-PassThru</span></span>
<span data-ttu-id="9d4a3-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9d4a3-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d4a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d4a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d4a3-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="9d4a3-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d4a3-124">-Confirm</span></span>
<span data-ttu-id="9d4a3-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4a3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d4a3-126">-WhatIf</span></span>
<span data-ttu-id="9d4a3-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d4a3-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4a3-129">CommonParameters</span></span>
<span data-ttu-id="9d4a3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d4a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4a3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d4a3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4a3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d4a3-132">INPUTS</span></span>

### <span data-ttu-id="9d4a3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9d4a3-133">System.String</span></span>

## <span data-ttu-id="9d4a3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d4a3-134">OUTPUTS</span></span>

### <span data-ttu-id="9d4a3-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d4a3-135">System.Boolean</span></span>

## <span data-ttu-id="9d4a3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d4a3-136">NOTES</span></span>

## <span data-ttu-id="9d4a3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d4a3-137">RELATED LINKS</span></span>

[<span data-ttu-id="9d4a3-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9d4a3-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="9d4a3-139">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9d4a3-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="9d4a3-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9d4a3-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


