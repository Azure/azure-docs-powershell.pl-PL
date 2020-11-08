---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054696"
---
# <span data-ttu-id="a63e3-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a63e3-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="a63e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a63e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a63e3-103">Tworzy środowisko Azure.</span><span class="sxs-lookup"><span data-stu-id="a63e3-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="a63e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a63e3-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a63e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a63e3-105">DESCRIPTION</span></span>
<span data-ttu-id="a63e3-106">Polecenie cmdlet **Add-AzureEnvironment** tworzy nowe niestandardowe środowisko konta platformy Azure i zapisuje je w profilu użytkownika mobilnego.</span><span class="sxs-lookup"><span data-stu-id="a63e3-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="a63e3-107">Polecenie cmdlet zwraca obiekt reprezentujący nowe środowisko.</span><span class="sxs-lookup"><span data-stu-id="a63e3-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="a63e3-108">Po ukończeniu polecenia możesz użyć środowiska w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a63e3-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="a63e3-109">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="a63e3-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="a63e3-110">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="a63e3-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="a63e3-111">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a63e3-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="a63e3-112">Tylko parametr **name** tego polecenia cmdlet jest obowiązkowy.</span><span class="sxs-lookup"><span data-stu-id="a63e3-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="a63e3-113">Jeśli pominięto parametr, jego wartość będzie równa null ($Null), a usługa korzystająca z tego punktu końcowego może nie działać prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="a63e3-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="a63e3-114">Aby dodać lub zmienić wartość właściwości środowisko, użyj polecenia cmdlet **Set-AzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="a63e3-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="a63e3-115">Uwaga: zmiana środowiska może spowodować niepowodzenie Twojego konta.</span><span class="sxs-lookup"><span data-stu-id="a63e3-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="a63e3-116">Zwykle środowiska są dodawane tylko w celu testowania lub rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="a63e3-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="a63e3-117">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a63e3-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a63e3-118">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a63e3-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a63e3-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a63e3-119">EXAMPLES</span></span>

### <span data-ttu-id="a63e3-120">Przykład 1: dodawanie środowiska platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a63e3-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="a63e3-121">To polecenie tworzy środowisko ContosoEnv Azure.</span><span class="sxs-lookup"><span data-stu-id="a63e3-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="a63e3-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a63e3-122">PARAMETERS</span></span>

### <span data-ttu-id="a63e3-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63e3-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="a63e3-124">Określa punkt końcowy uwierzytelniania usługi Azure Active Directory w nowym środowisku.</span><span class="sxs-lookup"><span data-stu-id="a63e3-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

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

### <span data-ttu-id="a63e3-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a63e3-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="a63e3-126">Określa identyfikator zasobu interfejsu API zarządzania, którego dostęp jest zarządzany przez usługę Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a63e3-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="a63e3-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="a63e3-127">-AdTenant</span></span>
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

### <span data-ttu-id="a63e3-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a63e3-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="a63e3-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a63e3-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="a63e3-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="a63e3-130">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="a63e3-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63e3-131">-GalleryEndpoint</span></span>
<span data-ttu-id="a63e3-132">Umożliwia określenie punktu końcowego galerii Menedżer zasobów Azure, w której są przechowywane szablony galerii grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="a63e3-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="a63e3-133">Aby uzyskać więcej informacji na temat grup zasobów platformy Azure i szablonów galerii, zobacz temat pomocy dla programu Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="a63e3-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

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

### <span data-ttu-id="a63e3-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63e3-134">-GraphEndpoint</span></span>
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

### <span data-ttu-id="a63e3-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="a63e3-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="a63e3-136">Określa adres URL portalu zarządzania Azure w nowym środowisku.</span><span class="sxs-lookup"><span data-stu-id="a63e3-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="a63e3-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a63e3-137">-Name</span></span>
<span data-ttu-id="a63e3-138">Określa nazwę środowiska.</span><span class="sxs-lookup"><span data-stu-id="a63e3-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="a63e3-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a63e3-139">This parameter is required.</span></span>
<span data-ttu-id="a63e3-140">Nie używaj nazw środowisk domyślnych, AzureCloud i AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="a63e3-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="a63e3-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="a63e3-141">-Profile</span></span>
<span data-ttu-id="a63e3-142">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a63e3-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a63e3-143">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a63e3-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a63e3-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="a63e3-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="a63e3-145">Określa adres URL plików ustawień publikowania dla konta.</span><span class="sxs-lookup"><span data-stu-id="a63e3-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="a63e3-146">Plik ustawień publikowania platformy Azure to plik XML, który zawiera informacje o Twoim koncie oraz certyfikat zarządzania, który umożliwia programowi Windows PowerShell logowanie się do konta platformy Azure w Twoim imieniu.</span><span class="sxs-lookup"><span data-stu-id="a63e3-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="a63e3-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63e3-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="a63e3-148">Określa punkt końcowy danych Menedżera zasobów platformy Azure, w tym dane dotyczące grup zasobów skojarzonych z kontem.</span><span class="sxs-lookup"><span data-stu-id="a63e3-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="a63e3-149">Aby uzyskać więcej informacji na temat Menedżera zasobów platformy Azure, zobacz [polecenia cmdlet Menedżera zasobów platformy Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) i [Używanie programu Windows PowerShell z Menedżerem zasobów](https://go.microsoft.com/fwlink/?LinkID=394767)  () https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="a63e3-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="a63e3-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63e3-150">-ServiceEndpoint</span></span>
<span data-ttu-id="a63e3-151">Określa adres URL punktu końcowego usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a63e3-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="a63e3-152">Punkt końcowy usługi Azure określa, czy aplikacja jest zarządzana przez platformę Global Azure, platformę Azure obsługiwaną przez firmę 21Vianet w Chinach lub prywatną instalację platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a63e3-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="a63e3-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a63e3-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="a63e3-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="a63e3-154">-StorageEndpoint</span></span>
<span data-ttu-id="a63e3-155">Określa domyślny punkt końcowy usług magazynowania w nowym środowisku.</span><span class="sxs-lookup"><span data-stu-id="a63e3-155">Specifies the default endpoint of storage services in the new environment.</span></span>

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

### <span data-ttu-id="a63e3-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a63e3-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="a63e3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63e3-157">CommonParameters</span></span>
<span data-ttu-id="a63e3-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63e3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63e3-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a63e3-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63e3-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63e3-160">INPUTS</span></span>

### <span data-ttu-id="a63e3-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a63e3-161">None</span></span>
<span data-ttu-id="a63e3-162">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="a63e3-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a63e3-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a63e3-163">OUTPUTS</span></span>

### <span data-ttu-id="a63e3-164">Microsoft. platformy windowsazure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a63e3-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="a63e3-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a63e3-165">NOTES</span></span>

## <span data-ttu-id="a63e3-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a63e3-166">RELATED LINKS</span></span>

[<span data-ttu-id="a63e3-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a63e3-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="a63e3-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a63e3-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="a63e3-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a63e3-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


