---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 4e937bd3ec1c40aaf4b3c1c188b157792c0030bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709107"
---
# <span data-ttu-id="50094-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="50094-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="50094-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50094-102">SYNOPSIS</span></span>
<span data-ttu-id="50094-103">Usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="50094-103">Removes a network security group.</span></span>

## <span data-ttu-id="50094-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50094-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50094-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50094-105">DESCRIPTION</span></span>
<span data-ttu-id="50094-106">Polecenie cmdlet **Remove-AzNetworkSecurityGroup** usuwa grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="50094-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="50094-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50094-107">EXAMPLES</span></span>

### <span data-ttu-id="50094-108">Przykład 1. Usuń grupę zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="50094-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="50094-109">To polecenie usuwa grupę zabezpieczeń o nazwie NSG-FrontEnd w grupie zasobów o nazwie TestRG.</span><span class="sxs-lookup"><span data-stu-id="50094-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="50094-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50094-110">PARAMETERS</span></span>

### <span data-ttu-id="50094-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50094-111">-AsJob</span></span>
<span data-ttu-id="50094-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="50094-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50094-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50094-113">-DefaultProfile</span></span>
<span data-ttu-id="50094-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50094-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50094-115">-Force</span><span class="sxs-lookup"><span data-stu-id="50094-115">-Force</span></span>
<span data-ttu-id="50094-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="50094-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50094-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50094-117">-Name</span></span>
<span data-ttu-id="50094-118">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="50094-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="50094-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50094-119">-PassThru</span></span>
<span data-ttu-id="50094-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="50094-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="50094-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="50094-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50094-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50094-122">-ResourceGroupName</span></span>
<span data-ttu-id="50094-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="50094-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="50094-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50094-124">-Confirm</span></span>
<span data-ttu-id="50094-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50094-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50094-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50094-126">-WhatIf</span></span>
<span data-ttu-id="50094-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50094-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50094-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="50094-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50094-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50094-129">CommonParameters</span></span>
<span data-ttu-id="50094-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50094-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50094-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50094-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50094-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50094-132">INPUTS</span></span>

### <span data-ttu-id="50094-133">System. String</span><span class="sxs-lookup"><span data-stu-id="50094-133">System.String</span></span>

## <span data-ttu-id="50094-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50094-134">OUTPUTS</span></span>

### <span data-ttu-id="50094-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50094-135">System.Boolean</span></span>

## <span data-ttu-id="50094-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50094-136">NOTES</span></span>

## <span data-ttu-id="50094-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50094-137">RELATED LINKS</span></span>

[<span data-ttu-id="50094-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="50094-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="50094-139">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="50094-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="50094-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="50094-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


