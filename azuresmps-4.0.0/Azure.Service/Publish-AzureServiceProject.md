---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054849"
---
# <span data-ttu-id="f4341-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f4341-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="f4341-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4341-102">SYNOPSIS</span></span>
<span data-ttu-id="f4341-103">Publikowanie bieżącej usługi na platformie Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="f4341-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4341-104">SYNTAX</span></span>

### <span data-ttu-id="f4341-105">PublishFromServiceDefinition (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4341-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f4341-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="f4341-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4341-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4341-107">DESCRIPTION</span></span>
<span data-ttu-id="f4341-108">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f4341-109">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f4341-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f4341-110">Polecenie cmdlet **Publish-AzureServiceProject** umożliwia publikowanie bieżącej usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="f4341-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="f4341-111">Możesz określić konfigurację publikowania (taką jak **subskrypcja** , **StorageAccountName** , **Lokalizacja** , miejsce **) w** wierszu polecenia lub w ustawieniach lokalnych za pomocą polecenia cmdlet **Set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="f4341-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="f4341-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4341-112">EXAMPLES</span></span>

### <span data-ttu-id="f4341-113">Przykład 1. publikowanie projektu usługi z wartościami domyślnymi</span><span class="sxs-lookup"><span data-stu-id="f4341-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="f4341-114">W tym przykładzie jest publikowana bieżąca usługa przy użyciu bieżących ustawień usługi i bieżącego profilu publikowania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="f4341-115">Przykład 2: Tworzenie pakietu wdrażania</span><span class="sxs-lookup"><span data-stu-id="f4341-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="f4341-116">W tym przykładzie przedstawiono tworzenie pliku pakietu wdrażania (cspkg) w katalogu usługi i nie można go publikować na platformie Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="f4341-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4341-117">PARAMETERS</span></span>

### <span data-ttu-id="f4341-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="f4341-118">-AffinityGroup</span></span>
<span data-ttu-id="f4341-119">Określa grupę koligacji, która ma być używana przez usługę.</span><span class="sxs-lookup"><span data-stu-id="f4341-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-120">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="f4341-120">-Configuration</span></span>
<span data-ttu-id="f4341-121">Określa plik konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="f4341-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="f4341-122">Jeśli określisz ten parametr, określ parametr *Package* .</span><span class="sxs-lookup"><span data-stu-id="f4341-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-123">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="f4341-123">-DeploymentName</span></span>
<span data-ttu-id="f4341-124">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f4341-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="f4341-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-126">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="f4341-126">-Launch</span></span>
<span data-ttu-id="f4341-127">Otwiera okno przeglądarki, w którym można wyświetlić aplikację po jej wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="f4341-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f4341-128">-Location</span></span>
<span data-ttu-id="f4341-129">Region, w którym aplikacja będzie hostowana.</span><span class="sxs-lookup"><span data-stu-id="f4341-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="f4341-130">Możliwe wartości:</span><span class="sxs-lookup"><span data-stu-id="f4341-130">Possible values are:</span></span> 
  
- <span data-ttu-id="f4341-131">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="f4341-131">Anywhere Asia</span></span>
- <span data-ttu-id="f4341-132">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="f4341-132">Anywhere Europe</span></span>
- <span data-ttu-id="f4341-133">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="f4341-133">Anywhere US</span></span>
- <span data-ttu-id="f4341-134">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="f4341-134">East Asia</span></span>
- <span data-ttu-id="f4341-135">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="f4341-135">East US</span></span>
- <span data-ttu-id="f4341-136">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="f4341-136">North Central US</span></span>
- <span data-ttu-id="f4341-137">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="f4341-137">North Europe</span></span>
- <span data-ttu-id="f4341-138">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="f4341-138">South Central US</span></span>
- <span data-ttu-id="f4341-139">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="f4341-139">Southeast Asia</span></span>
- <span data-ttu-id="f4341-140">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="f4341-140">West Europe</span></span>
- <span data-ttu-id="f4341-141">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="f4341-141">West US</span></span>
 
<span data-ttu-id="f4341-142">Jeśli nie określono lokalizacji, zostanie wykorzystana lokalizacja określona w ostatniej rozmowie z **poleceniem Set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="f4341-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="f4341-143">Jeśli żadna lokalizacja nie została kiedykolwiek określona, lokalizacja będzie wybierana losowo z lokalizacji "Północna Centrala Amerykańska" oraz "Południowa Centrala Amerykańska".</span><span class="sxs-lookup"><span data-stu-id="f4341-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-144">-Package</span><span class="sxs-lookup"><span data-stu-id="f4341-144">-Package</span></span>
<span data-ttu-id="f4341-145">Określa plik pakietu do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f4341-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="f4341-146">Określ plik lokalny z rozszerzeniem nazwy pliku cspkg lub identyfikatorem URI obiektu BLOB zawierającego pakiet.</span><span class="sxs-lookup"><span data-stu-id="f4341-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="f4341-147">Jeśli określisz ten parametr, nie określaj parametru *ServiceName* .</span><span class="sxs-lookup"><span data-stu-id="f4341-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4341-148">-Profile</span></span>
<span data-ttu-id="f4341-149">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4341-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4341-150">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f4341-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4341-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f4341-151">-ServiceName</span></span>
<span data-ttu-id="f4341-152">Określa nazwę, która ma być używana w usłudze podczas publikowania na platformie Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="f4341-153">Nazwa określa część etykiety w poddomenie cloudapp.net, która jest używana do zaadresowania usługi w systemie Windows Azure (czyli **name**. cloudapp.NET).</span><span class="sxs-lookup"><span data-stu-id="f4341-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="f4341-154">Każda nazwa określona podczas publikowania usługi zastępuje nazwę podaną w momencie utworzenia usługi.</span><span class="sxs-lookup"><span data-stu-id="f4341-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="f4341-155">(Zobacz polecenie cmdlet **New-AzureServiceProject** ).</span><span class="sxs-lookup"><span data-stu-id="f4341-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-156">-Slot</span><span class="sxs-lookup"><span data-stu-id="f4341-156">-Slot</span></span>
<span data-ttu-id="f4341-157">Miejsce wdrożenia, które ma być używane w tej usłudze.</span><span class="sxs-lookup"><span data-stu-id="f4341-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="f4341-158">Możliwe wartości to "przemieszczanie" i "produkcja".</span><span class="sxs-lookup"><span data-stu-id="f4341-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="f4341-159">Jeśli nie określono żadnego miejsca, zostanie użyte gniazdo podane w ostatniej rozmowie z Set-AzureDeploymentSlot.</span><span class="sxs-lookup"><span data-stu-id="f4341-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="f4341-160">Jeśli nie określono żadnego gniazda, zostanie użyte gniazdo "produkcja".</span><span class="sxs-lookup"><span data-stu-id="f4341-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f4341-161">-StorageAccountName</span></span>
<span data-ttu-id="f4341-162">Określa nazwę konta magazynu systemu Windows Azure, która ma być używana podczas publikowania usługi.</span><span class="sxs-lookup"><span data-stu-id="f4341-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="f4341-163">Ta wartość nie jest używana do momentu opublikowania usługi.</span><span class="sxs-lookup"><span data-stu-id="f4341-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="f4341-164">Jeśli ten parametr nie jest określony, wartość jest uzyskiwana z ostatniego polecenia **Set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="f4341-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="f4341-165">Jeśli nie określono żadnego konta magazynu, zostanie użyta nazwa konta magazynu odpowiadająca nazwie usługi.</span><span class="sxs-lookup"><span data-stu-id="f4341-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="f4341-166">Jeśli takie konto magazynu nie istnieje, polecenie cmdlet usiłuje utworzyć nowy.</span><span class="sxs-lookup"><span data-stu-id="f4341-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="f4341-167">Jednak próba może się nie powieść, jeśli konto magazynu zgodne z nazwą usługi istnieje w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f4341-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4341-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4341-168">CommonParameters</span></span>
<span data-ttu-id="f4341-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4341-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4341-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4341-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4341-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4341-171">INPUTS</span></span>

## <span data-ttu-id="f4341-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4341-172">OUTPUTS</span></span>

## <span data-ttu-id="f4341-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4341-173">NOTES</span></span>

## <span data-ttu-id="f4341-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4341-174">RELATED LINKS</span></span>

[<span data-ttu-id="f4341-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="f4341-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="f4341-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f4341-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


