---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 81eaa1f5c6e44586ae6ac9e5b6838f00063a9211
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890525"
---
# <span data-ttu-id="67849-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="67849-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="67849-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67849-102">SYNOPSIS</span></span>
<span data-ttu-id="67849-103">Tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="67849-103">Creates an application security group.</span></span>

## <span data-ttu-id="67849-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67849-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67849-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67849-105">DESCRIPTION</span></span>
<span data-ttu-id="67849-106">Polecenie cmdlet **New-AzApplicationSecurityGroup** tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="67849-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="67849-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67849-107">EXAMPLES</span></span>

### <span data-ttu-id="67849-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67849-108">Example 1</span></span>
```
PS C:\> New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="67849-109">W tym przykładzie jest tworzona Grupa zabezpieczeń aplikacji bez żadnych skojarzeń.</span><span class="sxs-lookup"><span data-stu-id="67849-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="67849-110">Po jego utworzeniu w grupie mogą wchodzić konfiguracje IP w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="67849-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="67849-111">Reguły bezpieczeństwa mogą również odwoływać się do grupy jako jej źródeł lub lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="67849-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="67849-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67849-112">PARAMETERS</span></span>

### <span data-ttu-id="67849-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67849-113">-AsJob</span></span>
<span data-ttu-id="67849-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="67849-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67849-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67849-115">-DefaultProfile</span></span>
<span data-ttu-id="67849-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67849-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67849-117">-Force</span><span class="sxs-lookup"><span data-stu-id="67849-117">-Force</span></span>
<span data-ttu-id="67849-118">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób.</span><span class="sxs-lookup"><span data-stu-id="67849-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="67849-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="67849-119">-Location</span></span>
<span data-ttu-id="67849-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="67849-120">The location.</span></span>

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

### <span data-ttu-id="67849-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67849-121">-Name</span></span>
<span data-ttu-id="67849-122">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="67849-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="67849-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67849-123">-ResourceGroupName</span></span>
<span data-ttu-id="67849-124">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="67849-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="67849-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="67849-125">-Tag</span></span>
<span data-ttu-id="67849-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="67849-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67849-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67849-127">-Confirm</span></span>
<span data-ttu-id="67849-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67849-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67849-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67849-129">-WhatIf</span></span>
<span data-ttu-id="67849-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67849-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67849-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67849-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67849-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67849-132">CommonParameters</span></span>
<span data-ttu-id="67849-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67849-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67849-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67849-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67849-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67849-135">INPUTS</span></span>

### <span data-ttu-id="67849-136">System. String</span><span class="sxs-lookup"><span data-stu-id="67849-136">System.String</span></span>
<span data-ttu-id="67849-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="67849-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="67849-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67849-138">OUTPUTS</span></span>

### <span data-ttu-id="67849-139">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="67849-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="67849-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67849-140">NOTES</span></span>

## <span data-ttu-id="67849-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67849-141">RELATED LINKS</span></span>

[<span data-ttu-id="67849-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="67849-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="67849-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="67849-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="67849-144">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67849-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="67849-145">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67849-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="67849-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="67849-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="67849-147">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="67849-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="67849-148">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="67849-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="67849-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="67849-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
