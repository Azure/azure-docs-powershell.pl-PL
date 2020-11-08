---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054933"
---
# <span data-ttu-id="742b0-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="742b0-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="742b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="742b0-102">SYNOPSIS</span></span>
<span data-ttu-id="742b0-103">Zmienia właściwości środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="742b0-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="742b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="742b0-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="742b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="742b0-105">DESCRIPTION</span></span>
<span data-ttu-id="742b0-106">Polecenie cmdlet **Set-AzureEnvironment** zmienia właściwości środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="742b0-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="742b0-107">Zwraca obiekt reprezentujący środowisko wraz z nowymi wartościami właściwości.</span><span class="sxs-lookup"><span data-stu-id="742b0-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="742b0-108">Parametr **name** służy do identyfikowania środowiska oraz innych parametrów umożliwiających zmianę wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="742b0-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="742b0-109">Nie można zmienić nazwy środowiska platformy Azure przy użyciu funkcji **Set-AzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="742b0-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="742b0-110">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="742b0-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="742b0-111">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="742b0-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="742b0-112">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="742b0-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="742b0-113">Uwaga: nie zmieniaj właściwości środowisk AzureCloud lub AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="742b0-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="742b0-114">Za pomocą tego polecenia cmdlet można zmieniać wartości środowiska prywatnego, które tworzysz.</span><span class="sxs-lookup"><span data-stu-id="742b0-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="742b0-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="742b0-115">EXAMPLES</span></span>

### <span data-ttu-id="742b0-116">Przykład 1: Zmienianie właściwości środowiska</span><span class="sxs-lookup"><span data-stu-id="742b0-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="742b0-117">To polecenie zmienia wartości właściwości **PublishSettingsFileUrl** i **StorageEndpoint** środowiska ContosoEnv.</span><span class="sxs-lookup"><span data-stu-id="742b0-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="742b0-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="742b0-118">PARAMETERS</span></span>

### <span data-ttu-id="742b0-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="742b0-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="742b0-120">Umożliwia zmianę punktu końcowego uwierzytelniania usługi Azure Active Directory na określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="742b0-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="742b0-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="742b0-122">Określa identyfikator zasobu interfejsu API zarządzania, którego dostęp jest zarządzany przez usługę Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="742b0-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="742b0-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="742b0-123">-AdTenant</span></span>
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

### <span data-ttu-id="742b0-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="742b0-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="742b0-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="742b0-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="742b0-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="742b0-126">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="742b0-127">-GalleryEndpoint</span></span>
<span data-ttu-id="742b0-128">Umożliwia zmianę punktu końcowego galerii Menedżera zasobów platformy Azure na określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="742b0-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="742b0-129">Punkt końcowy galerii to lokalizacja szablonów galerii grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="742b0-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="742b0-130">Aby uzyskać więcej informacji na temat grup zasobów platformy Azure i szablonów galerii, zobacz temat pomocy dla programu [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span><span class="sxs-lookup"><span data-stu-id="742b0-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="742b0-131">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="742b0-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="742b0-133">Zmienia adres URL portalu zarządzania platformy Azure na określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="742b0-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="742b0-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="742b0-134">-Name</span></span>
<span data-ttu-id="742b0-135">Umożliwia zidentyfikowanie środowiska, które jest zmieniane.</span><span class="sxs-lookup"><span data-stu-id="742b0-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="742b0-136">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="742b0-136">This parameter is required.</span></span>
<span data-ttu-id="742b0-137">W wartości parametru jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="742b0-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="742b0-138">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="742b0-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="742b0-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="742b0-139">-Profile</span></span>
<span data-ttu-id="742b0-140">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742b0-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="742b0-141">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="742b0-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="742b0-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="742b0-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="742b0-143">Zmienia adres URL plików ustawień publikowania w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="742b0-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="742b0-144">Plik ustawień publikowania platformy Azure to plik XML, który zawiera informacje o Twoim koncie oraz certyfikat zarządzania, który umożliwia programowi Windows PowerShell logowanie się do konta platformy Azure w Twoim imieniu.</span><span class="sxs-lookup"><span data-stu-id="742b0-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="742b0-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="742b0-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="742b0-146">Umożliwia zmianę punktu końcowego dla danych Menedżera zasobów platformy Azure, w tym danych dotyczących grup zasobów skojarzonych z kontem.</span><span class="sxs-lookup"><span data-stu-id="742b0-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="742b0-147">Aby uzyskać więcej informacji na temat Menedżera zasobów platformy Azure, zobacz [polecenia cmdlet Menedżera zasobów platformy Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) i [Używanie programu Windows PowerShell z Menedżerem zasobów](https://go.microsoft.com/fwlink/?LinkID=394767)  () https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="742b0-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="742b0-148">-ServiceEndpoint</span></span>
<span data-ttu-id="742b0-149">Zmienia adres URL punktu końcowego usługi platformy Azure w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="742b0-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="742b0-150">Punkt końcowy usługi Azure określa, czy aplikacja jest zarządzana przez platformę Global Azure, platformę Azure obsługiwaną przez firmę 21Vianet w Chinach lub prywatną instalację platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="742b0-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="742b0-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="742b0-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="742b0-152">-StorageEndpoint</span></span>
<span data-ttu-id="742b0-153">Zmienia domyślny punkt końcowy usług magazynu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="742b0-153">Changes the default endpoint of storage services in the specified environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="742b0-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="742b0-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="742b0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742b0-155">CommonParameters</span></span>
<span data-ttu-id="742b0-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742b0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742b0-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742b0-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742b0-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="742b0-158">INPUTS</span></span>

### <span data-ttu-id="742b0-159">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="742b0-159">None</span></span>
<span data-ttu-id="742b0-160">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="742b0-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="742b0-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="742b0-161">OUTPUTS</span></span>

### <span data-ttu-id="742b0-162">Microsoft. platformy windowsazure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="742b0-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="742b0-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="742b0-163">NOTES</span></span>

## <span data-ttu-id="742b0-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="742b0-164">RELATED LINKS</span></span>

[<span data-ttu-id="742b0-165">Dodaj-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="742b0-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="742b0-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="742b0-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="742b0-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="742b0-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


