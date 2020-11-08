---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055192"
---
# <span data-ttu-id="640e7-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640e7-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="640e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="640e7-102">SYNOPSIS</span></span>
<span data-ttu-id="640e7-103">Tworzy bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-103">Creates an application gateway.</span></span>

## <span data-ttu-id="640e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="640e7-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="640e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="640e7-105">DESCRIPTION</span></span>
<span data-ttu-id="640e7-106">Polecenie cmdlet **New-AzureApplicationGateway** tworzy bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="640e7-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="640e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="640e7-107">EXAMPLES</span></span>

### <span data-ttu-id="640e7-108">Przykład 1: Tworzenie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="640e7-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="640e7-109">To polecenie tworzy bramkę Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="640e7-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="640e7-110">Polecenie wdraża bramę w VirtualNetwork17 i w określonych podsieciach.</span><span class="sxs-lookup"><span data-stu-id="640e7-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="640e7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="640e7-111">PARAMETERS</span></span>

### <span data-ttu-id="640e7-112">— Opis</span><span class="sxs-lookup"><span data-stu-id="640e7-112">-Description</span></span>
<span data-ttu-id="640e7-113">Określa opis, który ten polecenie cmdlet przypisuje bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="640e7-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="640e7-114">-GatewaySize</span></span>
<span data-ttu-id="640e7-115">Określa rozmiar, który ten polecenie cmdlet przypisuje bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="640e7-116">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="640e7-116">Valid values are:</span></span>

- <span data-ttu-id="640e7-117">Mała</span><span class="sxs-lookup"><span data-stu-id="640e7-117">Small</span></span>
- <span data-ttu-id="640e7-118">Pożywkę</span><span class="sxs-lookup"><span data-stu-id="640e7-118">Medium</span></span>
- <span data-ttu-id="640e7-119">Większej</span><span class="sxs-lookup"><span data-stu-id="640e7-119">Large</span></span>

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

### <span data-ttu-id="640e7-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="640e7-120">-InstanceCount</span></span>
<span data-ttu-id="640e7-121">Określa liczbę wystąpień, które to polecenie cmdlet przypisuje bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="640e7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="640e7-122">-Name</span></span>
<span data-ttu-id="640e7-123">Określa nazwę nowej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-123">Specifies a name for the new application gateway.</span></span>

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

### <span data-ttu-id="640e7-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="640e7-124">-Profile</span></span>
<span data-ttu-id="640e7-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="640e7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="640e7-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="640e7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="640e7-127">-Podsieci</span><span class="sxs-lookup"><span data-stu-id="640e7-127">-Subnets</span></span>
<span data-ttu-id="640e7-128">Określa tablicę podsieci, w których to polecenie cmdlet wdraża bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640e7-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="640e7-129">-VnetName</span></span>
<span data-ttu-id="640e7-130">Określa sieć wirtualną, w której to polecenie cmdlet wdraża bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="640e7-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

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

### <span data-ttu-id="640e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640e7-131">CommonParameters</span></span>
<span data-ttu-id="640e7-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640e7-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640e7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640e7-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="640e7-134">INPUTS</span></span>

### <span data-ttu-id="640e7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="640e7-135">System.String</span></span>

## <span data-ttu-id="640e7-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="640e7-136">OUTPUTS</span></span>

### <span data-ttu-id="640e7-137">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="640e7-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="640e7-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="640e7-138">NOTES</span></span>

## <span data-ttu-id="640e7-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="640e7-139">RELATED LINKS</span></span>

[<span data-ttu-id="640e7-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640e7-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="640e7-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640e7-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="640e7-142">Start — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640e7-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="640e7-143">Zatrzymaj — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640e7-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="640e7-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="640e7-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
