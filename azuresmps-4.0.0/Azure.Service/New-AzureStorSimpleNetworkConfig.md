---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054481"
---
# <span data-ttu-id="5f05f-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="5f05f-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="5f05f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f05f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f05f-103">Przygotowowanie obiektu konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="5f05f-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="5f05f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f05f-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5f05f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f05f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f05f-106">Polecenie cmdlet **New-AzureStorSimpleNetworkConfig** umożliwia przygotowanie obiektu konfiguracji sieci do przechodzenia do polecenia cmdlet **Set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="5f05f-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="5f05f-107">Ustaw parametr *Controller0IPAddress* i parametr *Controller1IPAddress* tylko w interfejsie Data0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="5f05f-108">Data0 obsługuje tylko trzy ustawienia: *Controller0IPAddress* , *Controller1IPAdress* i *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="5f05f-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="5f05f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f05f-109">EXAMPLES</span></span>

### <span data-ttu-id="5f05f-110">Przykład 1: Konfigurowanie interfejsu Data0</span><span class="sxs-lookup"><span data-stu-id="5f05f-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="5f05f-111">To polecenie umożliwia utworzenie konfiguracji sieci dla interfejsu Data0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="5f05f-112">To polecenie określa parametry *Controller0IPv4Address* , *Controller1IPv4Address* i *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="5f05f-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="5f05f-113">To polecenie cmdlet umożliwia skonfigurowanie Data0 tylko dla tych trzech parametrów.</span><span class="sxs-lookup"><span data-stu-id="5f05f-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="5f05f-114">Przykład 2: Configuren interfejs inny niż Data0</span><span class="sxs-lookup"><span data-stu-id="5f05f-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="5f05f-115">To polecenie umożliwia skonfigurowanie interfejsu dane1.</span><span class="sxs-lookup"><span data-stu-id="5f05f-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="5f05f-116">Przykład 3: modyfikowanie konfiguracji urządzenia</span><span class="sxs-lookup"><span data-stu-id="5f05f-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="5f05f-117">Pierwsze polecenie tworzy konfigurację sieci dla interfejsu Data0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="5f05f-118">To polecenie określa parametry *Controller0IPv4Address* , *Controller1IPv4Address* i *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="5f05f-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="5f05f-119">Polecenie zapisuje wynik w zmiennej $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="5f05f-120">Drugie polecenie używa polecenia cmdlet **Get-AzureStorSimpleDevice** i podstawowego polecenia **WHERE-Object** w celu uzyskania urządzenia StorSimple online, a następnie zapisuje je w zmiennej $OnlineDevice.</span><span class="sxs-lookup"><span data-stu-id="5f05f-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="5f05f-121">Polecenie ostatnie modyfikuje konfigurację urządzenia o określonym IDENTYFIKATORze urządzenia przy użyciu polecenia cmdlet **Set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="5f05f-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="5f05f-122">W poleceniu jest używany obiekt konfiguracji, który jest tworzony przez bieżące polecenie cmdlet utworzone w pierwszym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="5f05f-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="5f05f-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f05f-123">PARAMETERS</span></span>

### <span data-ttu-id="5f05f-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="5f05f-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="5f05f-125">Określa adres IPv4 dla kontrolera 0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="5f05f-126">Ten parametr można określić tylko dla interfejsu Data0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-126">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="5f05f-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="5f05f-128">Określa adres IPv4 dla kontrolera 1.</span><span class="sxs-lookup"><span data-stu-id="5f05f-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="5f05f-129">Ten parametr można określić tylko dla interfejsu Data0.</span><span class="sxs-lookup"><span data-stu-id="5f05f-129">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="5f05f-130">-EnableCloud</span></span>
<span data-ttu-id="5f05f-131">Wskazuje, czy włączyć interfejs w chmurze.</span><span class="sxs-lookup"><span data-stu-id="5f05f-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="5f05f-132">-EnableIscsi</span></span>
<span data-ttu-id="5f05f-133">Wskazuje, czy włączyć funkcję Internet SCSI (ISCSI) dla interfejsu.</span><span class="sxs-lookup"><span data-stu-id="5f05f-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="5f05f-134">-InterfaceAlias</span></span>
<span data-ttu-id="5f05f-135">Określa alias interfejsu, dla którego są dostępne ustawienia tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f05f-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="5f05f-136">Prawidłowe wartości należą do przeData0 do Data5.</span><span class="sxs-lookup"><span data-stu-id="5f05f-136">Valid values are from Data0 to Data5.</span></span>

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

### <span data-ttu-id="5f05f-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="5f05f-137">-IPv4Address</span></span>
<span data-ttu-id="5f05f-138">Określa adres IPv4 interfejsu.</span><span class="sxs-lookup"><span data-stu-id="5f05f-138">Specifies the IPv4 address for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="5f05f-139">-IPv4Gateway</span></span>
<span data-ttu-id="5f05f-140">Określa adres IPv4 bramy.</span><span class="sxs-lookup"><span data-stu-id="5f05f-140">Specifies the IPv4 address of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="5f05f-141">-IPv4Netmask</span></span>
<span data-ttu-id="5f05f-142">Określa maskę sieci IPv4 dla interfejsu.</span><span class="sxs-lookup"><span data-stu-id="5f05f-142">Specifies the IPv4 netmask for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="5f05f-143">-IPv6Gateway</span></span>
<span data-ttu-id="5f05f-144">Określa bramę IPv6 dla interfejsu.</span><span class="sxs-lookup"><span data-stu-id="5f05f-144">Specifies the IPv6 gateway for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="5f05f-145">-IPv6Prefix</span></span>
<span data-ttu-id="5f05f-146">Określa prefiks IPv6 dla interfejsu.</span><span class="sxs-lookup"><span data-stu-id="5f05f-146">Specifies the IPv6 prefix for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f05f-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="5f05f-147">-Profile</span></span>
<span data-ttu-id="5f05f-148">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f05f-148">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5f05f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f05f-149">CommonParameters</span></span>
<span data-ttu-id="5f05f-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f05f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f05f-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f05f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f05f-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f05f-152">INPUTS</span></span>

### <span data-ttu-id="5f05f-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5f05f-153">None</span></span>

## <span data-ttu-id="5f05f-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f05f-154">OUTPUTS</span></span>

### <span data-ttu-id="5f05f-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="5f05f-155">NetworkConfig</span></span>
<span data-ttu-id="5f05f-156">To polecenie cmdlet zwraca obiekt NetworkConfig, który zawiera następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="5f05f-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="5f05f-157">**IsIscsiEnabled** ( **wartość logiczna** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="5f05f-158">**IsCloudEnabled** ( **wartość logiczna** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="5f05f-159">**Controller0IPv4Address** ( **adres_IP** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="5f05f-160">**Controller1IPv4Address** ( **adres_IP** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="5f05f-161">**IPv6Gateway** ( **adres_IP** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="5f05f-162">**IPv4Gateway** ( **adres_IP** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="5f05f-163">**IPv4Address** ( **adres_IP** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="5f05f-164">**IPv6Prefix** ( **ciąg** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="5f05f-165">**IPv4Netmask** ( **adres_IP** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="5f05f-166">**InterfaceAlias** ( **NetInterfaceId** )</span><span class="sxs-lookup"><span data-stu-id="5f05f-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="5f05f-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f05f-167">NOTES</span></span>

## <span data-ttu-id="5f05f-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f05f-168">RELATED LINKS</span></span>

[<span data-ttu-id="5f05f-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="5f05f-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="5f05f-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="5f05f-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


