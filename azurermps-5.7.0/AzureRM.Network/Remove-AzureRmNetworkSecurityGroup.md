---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 756d6c9f297faf133f38861879249ba281e65d53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526742"
---
# <span data-ttu-id="7eb0d-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7eb0d-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="7eb0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7eb0d-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb0d-103">Usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7eb0d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb0d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7eb0d-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb0d-106">Polecenie cmdlet **Remove-AzureRmNetworkSecurityGroup** usuwa grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="7eb0d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7eb0d-107">EXAMPLES</span></span>

### <span data-ttu-id="7eb0d-108">Przykład 1. Usuń grupę zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="7eb0d-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="7eb0d-109">To polecenie usuwa grupę zabezpieczeń o nazwie NSG-FrontEnd w grupie zasobów o nazwie TestRG.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="7eb0d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7eb0d-110">PARAMETERS</span></span>

### <span data-ttu-id="7eb0d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7eb0d-111">-AsJob</span></span>
<span data-ttu-id="7eb0d-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7eb0d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eb0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb0d-113">-DefaultProfile</span></span>
<span data-ttu-id="7eb0d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eb0d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7eb0d-115">-Force</span></span>
<span data-ttu-id="7eb0d-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7eb0d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7eb0d-117">-Name</span></span>
<span data-ttu-id="7eb0d-118">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7eb0d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eb0d-119">-PassThru</span></span>
<span data-ttu-id="7eb0d-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7eb0d-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7eb0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="7eb0d-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="7eb0d-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7eb0d-124">-Confirm</span></span>
<span data-ttu-id="7eb0d-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb0d-126">-WhatIf</span></span>
<span data-ttu-id="7eb0d-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb0d-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb0d-129">CommonParameters</span></span>
<span data-ttu-id="7eb0d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb0d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb0d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb0d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb0d-132">INPUTS</span></span>

### <span data-ttu-id="7eb0d-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7eb0d-133">None</span></span>
<span data-ttu-id="7eb0d-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7eb0d-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7eb0d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7eb0d-135">OUTPUTS</span></span>

## <span data-ttu-id="7eb0d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7eb0d-136">NOTES</span></span>

## <span data-ttu-id="7eb0d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb0d-137">RELATED LINKS</span></span>

[<span data-ttu-id="7eb0d-138">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7eb0d-138">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="7eb0d-139">Nowe — AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7eb0d-139">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="7eb0d-140">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7eb0d-140">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


