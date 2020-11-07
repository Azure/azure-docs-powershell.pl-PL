---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: ecda7c996bee6f707be27d3d58cf560ffaa50009
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890273"
---
# <span data-ttu-id="956cb-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="956cb-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="956cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="956cb-102">SYNOPSIS</span></span>
<span data-ttu-id="956cb-103">Usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="956cb-103">Removes a network security group.</span></span>

## <span data-ttu-id="956cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="956cb-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="956cb-105">DESCRIPTION</span></span>
<span data-ttu-id="956cb-106">Polecenie cmdlet **Remove-AzNetworkSecurityGroup** usuwa grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="956cb-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="956cb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="956cb-107">EXAMPLES</span></span>

### <span data-ttu-id="956cb-108">Przykład 1. Usuń grupę zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="956cb-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="956cb-109">To polecenie usuwa grupę zabezpieczeń o nazwie NSG-FrontEnd w grupie zasobów o nazwie TestRG.</span><span class="sxs-lookup"><span data-stu-id="956cb-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="956cb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="956cb-110">PARAMETERS</span></span>

### <span data-ttu-id="956cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="956cb-111">-AsJob</span></span>
<span data-ttu-id="956cb-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="956cb-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956cb-113">-DefaultProfile</span></span>
<span data-ttu-id="956cb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="956cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="956cb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="956cb-115">-Force</span></span>
<span data-ttu-id="956cb-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="956cb-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="956cb-117">-Name</span></span>
<span data-ttu-id="956cb-118">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="956cb-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="956cb-119">-PassThru</span></span>
<span data-ttu-id="956cb-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="956cb-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="956cb-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="956cb-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="956cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="956cb-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="956cb-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="956cb-124">-Confirm</span></span>
<span data-ttu-id="956cb-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="956cb-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956cb-126">-WhatIf</span></span>
<span data-ttu-id="956cb-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="956cb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956cb-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="956cb-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956cb-129">CommonParameters</span></span>
<span data-ttu-id="956cb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956cb-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956cb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956cb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="956cb-132">INPUTS</span></span>

## <span data-ttu-id="956cb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="956cb-133">OUTPUTS</span></span>

## <span data-ttu-id="956cb-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="956cb-134">NOTES</span></span>

## <span data-ttu-id="956cb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="956cb-135">RELATED LINKS</span></span>

[<span data-ttu-id="956cb-136">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="956cb-136">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="956cb-137">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="956cb-137">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="956cb-138">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="956cb-138">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


