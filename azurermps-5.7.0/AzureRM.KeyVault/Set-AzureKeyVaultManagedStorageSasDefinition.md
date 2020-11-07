---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 5a4c1effd1cbda4399e06f3b6db606cff87d8955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719177"
---
# <span data-ttu-id="8c0fa-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8c0fa-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8c0fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0fa-103">Ustawia definicję podpisu dostępu współużytkowanego (SAS) z magazynem kluczy dla danego magazynu kluczy zarządzanego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c0fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c0fa-104">SYNTAX</span></span>

### <span data-ttu-id="8c0fa-105">RawSas (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c0fa-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c0fa-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="8c0fa-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c0fa-119">Opis</span><span class="sxs-lookup"><span data-stu-id="8c0fa-119">DESCRIPTION</span></span>
<span data-ttu-id="8c0fa-120">Ustawia definicję podpisu dostępu udostępnionego (SAS) z danym magazynem kluczy zarządzanym kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="8c0fa-121">Ustawia również klucz tajny, którego można użyć w celu uzyskania tokenu SAS dla tej definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="8c0fa-122">Token SAS jest generowany przy użyciu tych parametrów i klucza aktywnego konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="8c0fa-123">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c0fa-123">EXAMPLES</span></span>

### <span data-ttu-id="8c0fa-124">Przykład 1: Ustawianie definicji SAS obiektu BLOB usługi ad hoc</span><span class="sxs-lookup"><span data-stu-id="8c0fa-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="8c0fa-125">Ustawia definicję zestawu SAS obiektu BLOB usługi ad hoc z kontem magazynu "sas1" zarządzanym magazynem kluczy "komputera1" w magazynie "vault1".</span><span class="sxs-lookup"><span data-stu-id="8c0fa-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="8c0fa-126">Przykład 2: Ustawianie definicji SAS konta ad hoc</span><span class="sxs-lookup"><span data-stu-id="8c0fa-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="8c0fa-127">Ustawia definicję "sas1" obiektu BLOB ad hoc z kontem magazynu zarządzania magazynu kluczy "komputera1" w magazynie "vault1".</span><span class="sxs-lookup"><span data-stu-id="8c0fa-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="8c0fa-128">Przykład 3: Ustawianie definicji SAS za pomocą obiektu Hashtable</span><span class="sxs-lookup"><span data-stu-id="8c0fa-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="8c0fa-129">Ustawia definicję "sas1" w obiekcie blob ad hoc z kontem magazynu zarządzanym magazynem kluczy "komputera1" w magazynie "vault1" przy użyciu obiektu Hashtable.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="8c0fa-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c0fa-130">PARAMETERS</span></span>

### <span data-ttu-id="8c0fa-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c0fa-131">-AccountName</span></span>
<span data-ttu-id="8c0fa-132">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="8c0fa-133">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c0fa-134">-ApiVersion</span></span>
<span data-ttu-id="8c0fa-135">Określa wersję usługi magazynu, która ma być używana do wykonania żądania przy użyciu identyfikatora URI SAS konta.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-136">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="8c0fa-136">-Blob</span></span>
<span data-ttu-id="8c0fa-137">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="8c0fa-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-138">-Kontener</span><span class="sxs-lookup"><span data-stu-id="8c0fa-138">-Container</span></span>
<span data-ttu-id="8c0fa-139">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="8c0fa-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0fa-140">-DefaultProfile</span></span>
<span data-ttu-id="8c0fa-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8c0fa-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c0fa-142">-Disable</span><span class="sxs-lookup"><span data-stu-id="8c0fa-142">-Disable</span></span>
<span data-ttu-id="8c0fa-143">Wyłącza używanie definicji SAS do generowania tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="8c0fa-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8c0fa-144">-EndPartitionKey</span></span>
<span data-ttu-id="8c0fa-145">Koniec klucza partycji</span><span class="sxs-lookup"><span data-stu-id="8c0fa-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="8c0fa-146">-EndRowKey</span></span>
<span data-ttu-id="8c0fa-147">Klucz końca wiersza</span><span class="sxs-lookup"><span data-stu-id="8c0fa-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8c0fa-148">-IPAddressOrRange</span></span>
<span data-ttu-id="8c0fa-149">Adres IP lub wykaz ACL zakresu adresów IP (lista kontroli dostępu) żądania, które zostałyby zaakceptowane przez usługę Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c0fa-150">-Name</span></span>
<span data-ttu-id="8c0fa-151">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-151">Storage sas definition name.</span></span> <span data-ttu-id="8c0fa-152">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8c0fa-153">-Parameter</span></span>
<span data-ttu-id="8c0fa-154">Parametry definicji SAS, które zostaną użyte do utworzenia tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-155">-Path</span><span class="sxs-lookup"><span data-stu-id="8c0fa-155">-Path</span></span>
<span data-ttu-id="8c0fa-156">Ścieżka do pliku w chmurze, w której ma być generowany token SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-157">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="8c0fa-157">-Permission</span></span>
<span data-ttu-id="8c0fa-158">Pozwolenia.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-158">Permission.</span></span> <span data-ttu-id="8c0fa-159">Do wartości należą: "kwerenda", "Dodaj", "Update", "Process"</span><span class="sxs-lookup"><span data-stu-id="8c0fa-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-160">-Policy</span><span class="sxs-lookup"><span data-stu-id="8c0fa-160">-Policy</span></span>
<span data-ttu-id="8c0fa-161">Identyfikator zasad</span><span class="sxs-lookup"><span data-stu-id="8c0fa-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-162">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="8c0fa-162">-Protocol</span></span>
<span data-ttu-id="8c0fa-163">Protokołu można użyć w żądaniu z tokenem SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-164">-Queue</span><span class="sxs-lookup"><span data-stu-id="8c0fa-164">-Queue</span></span>
<span data-ttu-id="8c0fa-165">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="8c0fa-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8c0fa-166">-ResourceType</span></span>
<span data-ttu-id="8c0fa-167">Typy zasobów, których dotyczy ten token SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="8c0fa-168">Do wartości należą: "usługa", "kontener", "obiekt"</span><span class="sxs-lookup"><span data-stu-id="8c0fa-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-169">-Service</span><span class="sxs-lookup"><span data-stu-id="8c0fa-169">-Service</span></span>
<span data-ttu-id="8c0fa-170">Typy usług, których dotyczy ten token SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="8c0fa-171">Do wartości należą: "BLOB", "File", "queued", "Table"</span><span class="sxs-lookup"><span data-stu-id="8c0fa-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-172">-Share</span><span class="sxs-lookup"><span data-stu-id="8c0fa-172">-Share</span></span>
<span data-ttu-id="8c0fa-173">Nazwa udziału</span><span class="sxs-lookup"><span data-stu-id="8c0fa-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="8c0fa-174">-SharedAccessHeader</span></span>
<span data-ttu-id="8c0fa-175">Określa parametry zapytania, które mają zastąpić nagłówki odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8c0fa-176">-StartPartitionKey</span></span>
<span data-ttu-id="8c0fa-177">Klucz partycji początkowej</span><span class="sxs-lookup"><span data-stu-id="8c0fa-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="8c0fa-178">-StartRowKey</span></span>
<span data-ttu-id="8c0fa-179">Klucz wiersza rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="8c0fa-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-180">-Table</span><span class="sxs-lookup"><span data-stu-id="8c0fa-180">-Table</span></span>
<span data-ttu-id="8c0fa-181">Nazwa tabeli</span><span class="sxs-lookup"><span data-stu-id="8c0fa-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c0fa-182">-Tag</span></span>
<span data-ttu-id="8c0fa-183">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c0fa-184">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="8c0fa-184">For example:</span></span>

<span data-ttu-id="8c0fa-185">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="8c0fa-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="8c0fa-186">-TargetStorageVersion</span></span>
<span data-ttu-id="8c0fa-187">Określa wersję usługi podpisanej, która ma być używana do uwierzytelniania żądań wykonywanych za pomocą tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="8c0fa-188">-ValidityPeriod</span></span>
<span data-ttu-id="8c0fa-189">Okres ważności, który zostanie wykorzystany do ustawienia czasu wygaśnięcia tokenu SAS od momentu jego wygenerowania</span><span class="sxs-lookup"><span data-stu-id="8c0fa-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-190">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="8c0fa-190">-VaultName</span></span>
<span data-ttu-id="8c0fa-191">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-191">Vault name.</span></span>
<span data-ttu-id="8c0fa-192">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0fa-193">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c0fa-193">-Confirm</span></span>
<span data-ttu-id="8c0fa-194">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c0fa-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c0fa-195">-WhatIf</span></span>
<span data-ttu-id="8c0fa-196">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c0fa-197">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c0fa-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0fa-198">CommonParameters</span></span>
<span data-ttu-id="8c0fa-199">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0fa-200">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c0fa-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0fa-201">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c0fa-201">INPUTS</span></span>

### <span data-ttu-id="8c0fa-202">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8c0fa-202">None</span></span>
<span data-ttu-id="8c0fa-203">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8c0fa-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c0fa-204">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c0fa-204">OUTPUTS</span></span>

### <span data-ttu-id="8c0fa-205">Microsoft. Azure. Commands. platforming. models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8c0fa-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8c0fa-206">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c0fa-206">NOTES</span></span>

## <span data-ttu-id="8c0fa-207">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c0fa-207">RELATED LINKS</span></span>

[<span data-ttu-id="8c0fa-208">Azureâ € ‹ RM. â € ‹ keyâ € ‹</span><span class="sxs-lookup"><span data-stu-id="8c0fa-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
