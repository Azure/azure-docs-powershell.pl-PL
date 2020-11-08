---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054766"
---
# <span data-ttu-id="bee2f-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="bee2f-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="bee2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bee2f-102">SYNOPSIS</span></span>
<span data-ttu-id="bee2f-103">Dodaje lub modyfikuje regułę zabezpieczeń sieci w grupie zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="bee2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bee2f-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bee2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bee2f-105">DESCRIPTION</span></span>
<span data-ttu-id="bee2f-106">Polecenie cmdlet **Set-AzureNetworkSecurityRule** umożliwia dodanie lub zmodyfikowanie reguły zabezpieczeń sieci Azure w grupie zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="bee2f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bee2f-107">EXAMPLES</span></span>

## <span data-ttu-id="bee2f-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bee2f-108">PARAMETERS</span></span>

### <span data-ttu-id="bee2f-109">-Action</span><span class="sxs-lookup"><span data-stu-id="bee2f-109">-Action</span></span>
<span data-ttu-id="bee2f-110">Określa akcję dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="bee2f-111">Prawidłowe wartości to: Allow i Deny.</span><span class="sxs-lookup"><span data-stu-id="bee2f-111">Valid values are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bee2f-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="bee2f-113">Określa adres IP Classless subdomain Routing (CIDR) dla docelowego zakresu adresów IP dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="bee2f-114">Gwiazdka (\*) określa dowolny adres IP.</span><span class="sxs-lookup"><span data-stu-id="bee2f-114">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="bee2f-115">-DestinationPortRange</span></span>
<span data-ttu-id="bee2f-116">Określa zakres portów docelowych dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="bee2f-117">Prawidłowe wartości zawierają liczby całkowite z zakresu od 0 do 65535.</span><span class="sxs-lookup"><span data-stu-id="bee2f-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="bee2f-118">Możesz określić pojedynczą wartość lub określić zakres w formacie LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="bee2f-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="bee2f-119">Łącznik oddziela dwie wartości.</span><span class="sxs-lookup"><span data-stu-id="bee2f-119">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bee2f-120">-Name</span></span>
<span data-ttu-id="bee2f-121">Określa nazwę reguły zabezpieczeń sieci, którą to polecenie cmdlet dodaje lub modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="bee2f-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bee2f-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bee2f-123">Określa grupę zabezpieczeń sieci, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="bee2f-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="bee2f-124">Aby uzyskać obiekt **INetworkSecurityGroup** , użyj polecenia cmdlet Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="bee2f-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-125">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="bee2f-125">-Priority</span></span>
<span data-ttu-id="bee2f-126">Określa priorytet reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="bee2f-127">Prawidłowe wartości to: liczba całkowita z zakresu od 100 do 4096.</span><span class="sxs-lookup"><span data-stu-id="bee2f-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="bee2f-128">-Profile</span></span>
<span data-ttu-id="bee2f-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee2f-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bee2f-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bee2f-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-131">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="bee2f-131">-Protocol</span></span>
<span data-ttu-id="bee2f-132">Określa protokół dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="bee2f-133">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="bee2f-133">Valid values are:</span></span> 

- <span data-ttu-id="bee2f-134">PROTOKOŁ</span><span class="sxs-lookup"><span data-stu-id="bee2f-134">TCP</span></span> 
- <span data-ttu-id="bee2f-135">OBSŁUGIWANE</span><span class="sxs-lookup"><span data-stu-id="bee2f-135">UDP</span></span> 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bee2f-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="bee2f-137">Określa adres CIDR źródłowego zakresu adresów IP dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="bee2f-138">Gwiazdka (\*) określa dowolny adres IP.</span><span class="sxs-lookup"><span data-stu-id="bee2f-138">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="bee2f-139">-SourcePortRange</span></span>
<span data-ttu-id="bee2f-140">Określa zakres portów źródłowych dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="bee2f-141">Prawidłowe wartości zawierają liczby całkowite z zakresu od 0 do 65535.</span><span class="sxs-lookup"><span data-stu-id="bee2f-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="bee2f-142">Możesz określić pojedynczą wartość lub określić zakres w formacie LowerNumber-HigherNumber.</span><span class="sxs-lookup"><span data-stu-id="bee2f-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="bee2f-143">Łącznik oddziela dwie wartości.</span><span class="sxs-lookup"><span data-stu-id="bee2f-143">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-144">-Type</span><span class="sxs-lookup"><span data-stu-id="bee2f-144">-Type</span></span>
<span data-ttu-id="bee2f-145">Określa typ połączenia dla reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bee2f-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="bee2f-146">Prawidłowe wartości to: przychodzące i wychodzące.</span><span class="sxs-lookup"><span data-stu-id="bee2f-146">Valid values are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee2f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee2f-147">CommonParameters</span></span>
<span data-ttu-id="bee2f-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee2f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee2f-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee2f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee2f-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee2f-150">INPUTS</span></span>

## <span data-ttu-id="bee2f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bee2f-151">OUTPUTS</span></span>

## <span data-ttu-id="bee2f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bee2f-152">NOTES</span></span>

## <span data-ttu-id="bee2f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bee2f-153">RELATED LINKS</span></span>

[<span data-ttu-id="bee2f-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="bee2f-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


