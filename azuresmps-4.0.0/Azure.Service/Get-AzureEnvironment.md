---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055318"
---
# <span data-ttu-id="3f004-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f004-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="3f004-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f004-102">SYNOPSIS</span></span>
<span data-ttu-id="3f004-103">Pobiera środowiska Azure</span><span class="sxs-lookup"><span data-stu-id="3f004-103">Gets Azure environments</span></span>

## <span data-ttu-id="3f004-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f004-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f004-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f004-105">DESCRIPTION</span></span>
<span data-ttu-id="3f004-106">Polecenie cmdlet **Get-AzureEnvironment** pobiera środowiska platformy Azure dostępne dla programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3f004-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="3f004-107">Środowisko platformy Azure niezależne wdrożenie platformy Microsoft Azure, takiej jak AzureCloud dla usługi Azure i AzureChinaCloud dla platformy Azure obsługiwanej przez firmę 21Vianet w Chinach.</span><span class="sxs-lookup"><span data-stu-id="3f004-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="3f004-108">Lokalne środowiska platformy Azure można też tworzyć, korzystając z pakietu Azure i poleceń cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="3f004-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="3f004-109">Aby uzyskać więcej informacji, zobacz [pakiet Azure](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3f004-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="3f004-110">Polecenie cmdlet **Get-AzureEnvironment** pobiera środowiska z pliku danych abonamentu, a nie z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f004-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="3f004-111">Jeśli plik danych subskrypcji jest nieaktualny, uruchom polecenie cmdlet **Add-AzureAccount** lub **Import-PublishSettingsFile** , aby je odświeżyć.</span><span class="sxs-lookup"><span data-stu-id="3f004-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="3f004-112">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f004-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3f004-113">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3f004-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="3f004-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f004-114">EXAMPLES</span></span>

### <span data-ttu-id="3f004-115">Przykład 1. Pobierz wszystkie środowiska</span><span class="sxs-lookup"><span data-stu-id="3f004-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="3f004-116">To polecenie uzyskuje wszystkie środowiska dostępne w programie Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3f004-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="3f004-117">Przykład 2: uzyskiwanie środowiska według nazwy</span><span class="sxs-lookup"><span data-stu-id="3f004-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="3f004-118">W tym przykładzie jest pobierany środowisko AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="3f004-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="3f004-119">Przykład 3: pobieranie wszystkich właściwości we wszystkich środowiskach</span><span class="sxs-lookup"><span data-stu-id="3f004-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="3f004-120">To polecenie pobiera wszystkie właściwości wszystkich środowisk.</span><span class="sxs-lookup"><span data-stu-id="3f004-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="3f004-121">W poleceniu użyto polecenia cmdlet **Get-AzureEnvironment** w celu uzyskania wszystkich środowisk Azure dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="3f004-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="3f004-122">Następnie korzysta z polecenia cmdlet **ForEach-Object** , aby uruchomić polecenie **Get-AzureEnvironment** z parametrem **name** w każdym środowisku.</span><span class="sxs-lookup"><span data-stu-id="3f004-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="3f004-123">Wartość parametru **name** to właściwość **EnvironmentName** każdego środowiska.</span><span class="sxs-lookup"><span data-stu-id="3f004-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="3f004-124">Bez parametrów polecenie **Get-AzureEnvironment** pobiera tylko wybrane właściwości środowiska.</span><span class="sxs-lookup"><span data-stu-id="3f004-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="3f004-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f004-125">PARAMETERS</span></span>

### <span data-ttu-id="3f004-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f004-126">-Name</span></span>
<span data-ttu-id="3f004-127">Pobiera tylko określone środowisko.</span><span class="sxs-lookup"><span data-stu-id="3f004-127">Gets only the specified environment.</span></span>
<span data-ttu-id="3f004-128">Wpisz nazwę środowiska.</span><span class="sxs-lookup"><span data-stu-id="3f004-128">Type the environment name.</span></span>
<span data-ttu-id="3f004-129">W wartości parametru jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="3f004-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="3f004-130">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="3f004-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="3f004-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="3f004-131">-Profile</span></span>
<span data-ttu-id="3f004-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f004-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3f004-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3f004-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f004-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f004-134">CommonParameters</span></span>
<span data-ttu-id="3f004-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f004-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f004-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f004-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f004-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f004-137">INPUTS</span></span>

### <span data-ttu-id="3f004-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3f004-138">None</span></span>
<span data-ttu-id="3f004-139">Możesz popotokować dane wejściowe tego polecenia cmdlet, korzystając z nazwy właściwości, ale nie według wartości.</span><span class="sxs-lookup"><span data-stu-id="3f004-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3f004-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f004-140">OUTPUTS</span></span>

### <span data-ttu-id="3f004-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="3f004-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="3f004-142">Domyślnie funkcja **Get-AzureEnvironment** zwraca obiekt niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="3f004-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="3f004-143">Microsoft. platformy windowsazure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f004-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="3f004-144">Po uruchomieniu funkcji **Get-AzureEnvironment** z parametrem **name** zwraca obiekt  **WindowsAzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="3f004-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="3f004-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f004-145">NOTES</span></span>

## <span data-ttu-id="3f004-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f004-146">RELATED LINKS</span></span>

[<span data-ttu-id="3f004-147">Dodaj-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="3f004-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="3f004-148">Dodaj-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f004-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="3f004-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3f004-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="3f004-150">Import — AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3f004-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="3f004-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f004-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="3f004-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f004-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


