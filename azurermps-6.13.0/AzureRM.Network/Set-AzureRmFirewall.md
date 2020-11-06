---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524378"
---
# <span data-ttu-id="c63f1-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="c63f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c63f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c63f1-103">Umożliwia zapisanie zmodyfikowanej zapory.</span><span class="sxs-lookup"><span data-stu-id="c63f1-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c63f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c63f1-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c63f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c63f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c63f1-106">Polecenie cmdlet **Set-AzureRmFirewall** aktualizuje zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c63f1-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="c63f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c63f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c63f1-108">1: priorytet aktualizacji kolekcji reguł aplikacji zapory</span><span class="sxs-lookup"><span data-stu-id="c63f1-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="c63f1-109">W tym przykładzie Zaktualizowano priorytet istniejącej kolekcji reguł w zaporze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c63f1-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="c63f1-110">Zakładając, że Zapora platformy Azure "AzureFirewall" w grupie zasobów "RG" zawiera kolekcję reguł aplikacji o nazwie "ruleCollectionName", powyższe polecenia zmienią priorytet kolekcji reguł, a następnie zaktualizują zaporę systemu Azure później.</span><span class="sxs-lookup"><span data-stu-id="c63f1-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="c63f1-111">Bez polecenia Set-AzureRmFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.</span><span class="sxs-lookup"><span data-stu-id="c63f1-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="c63f1-112">2: Tworzenie zapory na platformie Azure i Konfigurowanie kolekcji reguł aplikacji później</span><span class="sxs-lookup"><span data-stu-id="c63f1-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="c63f1-113">W tym przykładzie Zapora jest tworzona jako pierwsza bez żadnych kolekcji reguł aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c63f1-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="c63f1-114">Po utworzeniu zestawu reguł aplikacji i kolekcji reguł aplikacji obiekt firewall jest modyfikowany w pamięci bez wpływu na rzeczywistą konfigurację w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c63f1-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="c63f1-115">Aby zmiany zostały odzwierciedlone w chmurze, należy najpierw wywołać Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="c63f1-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="c63f1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c63f1-116">PARAMETERS</span></span>

### <span data-ttu-id="c63f1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c63f1-117">-AsJob</span></span>
<span data-ttu-id="c63f1-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c63f1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c63f1-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-119">-AzureFirewall</span></span>
<span data-ttu-id="c63f1-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c63f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63f1-121">-DefaultProfile</span></span>
<span data-ttu-id="c63f1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c63f1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c63f1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c63f1-123">-Confirm</span></span>
<span data-ttu-id="c63f1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63f1-125">-WhatIf</span></span>
<span data-ttu-id="c63f1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63f1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c63f1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c63f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63f1-128">CommonParameters</span></span>
<span data-ttu-id="c63f1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63f1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c63f1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63f1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c63f1-131">INPUTS</span></span>

### <span data-ttu-id="c63f1-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-132">PSAzureFirewall</span></span>
<span data-ttu-id="c63f1-133">Parametr "AzureFirewall" akceptuje wartość typu "PSAzureFirewall" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c63f1-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="c63f1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c63f1-134">OUTPUTS</span></span>

### <span data-ttu-id="c63f1-135">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c63f1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c63f1-136">NOTES</span></span>

## <span data-ttu-id="c63f1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c63f1-137">RELATED LINKS</span></span>

[<span data-ttu-id="c63f1-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="c63f1-139">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="c63f1-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c63f1-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
