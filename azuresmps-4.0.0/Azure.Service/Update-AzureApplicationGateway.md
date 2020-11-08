---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054810"
---
# <span data-ttu-id="8aa9f-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aa9f-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="8aa9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8aa9f-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa9f-103">Umożliwia zaktualizowanie bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-103">Updates an application gateway.</span></span>

## <span data-ttu-id="8aa9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8aa9f-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8aa9f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8aa9f-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa9f-106">Polecenie cmdlet **Update-AzureApplicationGateway** umożliwia zaktualizowanie istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="8aa9f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8aa9f-107">EXAMPLES</span></span>

### <span data-ttu-id="8aa9f-108">Przykład 1: modyfikowanie bramy aplikacji przy użyciu jej nazwy</span><span class="sxs-lookup"><span data-stu-id="8aa9f-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="8aa9f-109">Pierwsze polecenie zatrzymuje bramkę Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="8aa9f-110">Aby można było zmodyfikować sieć wirtualną lub podsieci, Brama aplikacji musi zostać zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="8aa9f-111">Drugie polecenie modyfikuje podsieć wirtualną i podsieci dla bramy Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="8aa9f-112">Przykład 2: modyfikowanie dodatkowych właściwości bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8aa9f-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="8aa9f-113">To polecenie modyfikuje liczbę wystąpień, rozmiar bramy i opis bramy Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="8aa9f-114">To polecenie nie powoduje zmiany sieci wirtualnej ani podsieci dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="8aa9f-115">Dlatego nie trzeba zatrzymywać bramy aplikacji przed uruchomieniem tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="8aa9f-116">Przykład 3: modyfikowanie bramy aplikacji za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="8aa9f-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="8aa9f-117">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway06 przy użyciu polecenia cmdlet **Get-AzureApplicationGateway** .</span><span class="sxs-lookup"><span data-stu-id="8aa9f-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="8aa9f-118">Polecenie zapisuje je w zmiennej $ApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="8aa9f-119">Drugie polecenie przypisuje Właściwość **GatewaySize** wartość średnia.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="8aa9f-120">Polecenie ostatnie przekazuje zaktualizowaną $ApplicationGateway do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="8aa9f-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8aa9f-121">PARAMETERS</span></span>

### <span data-ttu-id="8aa9f-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="8aa9f-122">-Description</span></span>
<span data-ttu-id="8aa9f-123">Określa opis, który ten polecenie cmdlet przypisuje bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa9f-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="8aa9f-124">-GatewaySize</span></span>
<span data-ttu-id="8aa9f-125">Określa rozmiar, który ten polecenie cmdlet przypisuje bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="8aa9f-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8aa9f-126">Valid values are:</span></span>

- <span data-ttu-id="8aa9f-127">Mała</span><span class="sxs-lookup"><span data-stu-id="8aa9f-127">Small</span></span>
- <span data-ttu-id="8aa9f-128">Pożywkę</span><span class="sxs-lookup"><span data-stu-id="8aa9f-128">Medium</span></span>
- <span data-ttu-id="8aa9f-129">Większej</span><span class="sxs-lookup"><span data-stu-id="8aa9f-129">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa9f-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="8aa9f-130">-InstanceCount</span></span>
<span data-ttu-id="8aa9f-131">Określa liczbę wystąpień, które to polecenie cmdlet przypisuje bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa9f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8aa9f-132">-Name</span></span>
<span data-ttu-id="8aa9f-133">Określa nazwę bramy aplikacji, która jest aktualizowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8aa9f-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="8aa9f-134">-Profile</span></span>
<span data-ttu-id="8aa9f-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8aa9f-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8aa9f-137">-Podsieci</span><span class="sxs-lookup"><span data-stu-id="8aa9f-137">-Subnets</span></span>
<span data-ttu-id="8aa9f-138">Określa tablicę podsieci, w których to polecenie cmdlet wdraża bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="8aa9f-139">Nie można aktualizować podsieci, gdy Brama aplikacji jest uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="8aa9f-140">Aby zatrzymać bramę Application Gateway, użyj polecenia cmdlet Stop-AzureApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa9f-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="8aa9f-141">-VnetName</span></span>
<span data-ttu-id="8aa9f-142">Określa sieć wirtualną, w której to polecenie cmdlet wdraża bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="8aa9f-143">Nie można zaktualizować sieci wirtualnej, gdy Brama Application Gateway jest uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="8aa9f-144">Aby zatrzymać bramę Application Gateway, użyj pola **stop-AzureApplicationGateway**.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa9f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa9f-145">CommonParameters</span></span>
<span data-ttu-id="8aa9f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa9f-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aa9f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa9f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aa9f-148">INPUTS</span></span>

### <span data-ttu-id="8aa9f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8aa9f-149">System.String</span></span>

## <span data-ttu-id="8aa9f-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8aa9f-150">OUTPUTS</span></span>

### <span data-ttu-id="8aa9f-151">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8aa9f-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="8aa9f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8aa9f-152">NOTES</span></span>

## <span data-ttu-id="8aa9f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aa9f-153">RELATED LINKS</span></span>

[<span data-ttu-id="8aa9f-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aa9f-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="8aa9f-155">Nowe — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aa9f-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="8aa9f-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aa9f-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="8aa9f-157">Start — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aa9f-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="8aa9f-158">Zatrzymaj — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8aa9f-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
