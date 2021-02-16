---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185483"
---
# <span data-ttu-id="ddc7e-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ddc7e-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="ddc7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc7e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc7e-103">Ustawia definicję podpisu SAS (Shared Access Signature) z magazynem kluczy dla danego zarządzanego konta magazynu usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ddc7e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddc7e-104">SYNTAX</span></span>

### <span data-ttu-id="ddc7e-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ddc7e-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc7e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ddc7e-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddc7e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddc7e-107">DESCRIPTION</span></span>
<span data-ttu-id="ddc7e-108">Ustawia definicję podpisu SAS (Shared Access Signature) z danym kontem magazynu kluczy zarządzanym przez usługę Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="ddc7e-109">Ustawia to również klucz tajny, którego można użyć do uzyskania tokenu SAS na tę definicję SAS.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="ddc7e-110">Token SAS jest generowany przy użyciu tych parametrów i aktywnego klucza zarządzanego konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ddc7e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddc7e-111">EXAMPLES</span></span>

### <span data-ttu-id="ddc7e-112">Przykład 1. Ustawianie definicji SAS typu konta i uzyskiwanie na jej podstawie bieżącego tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="ddc7e-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="ddc7e-113">Ustawia definicję SAS konta "accountsas" na koncie magazynu zarządzanego przez usługę KeyVault "mysa" w magazynie "mykv".</span><span class="sxs-lookup"><span data-stu-id="ddc7e-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="ddc7e-114">W szczególności powyższy ciąg wykonuje następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="ddc7e-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="ddc7e-115">otrzymuje (istniejące) konto magazynu</span><span class="sxs-lookup"><span data-stu-id="ddc7e-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="ddc7e-116">pobiera (istniejący) magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="ddc7e-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="ddc7e-117">dodaje konto magazynu zarządzanego przez usługę KeyVault do magazynu, ustawiając klucz Klucz1 jako klucz aktywny i z okresem 180 dni</span><span class="sxs-lookup"><span data-stu-id="ddc7e-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="ddc7e-118">ustawia kontekst miejsca do magazynowania dla określonego konta magazynu przy użyciu klawisza Klucz1</span><span class="sxs-lookup"><span data-stu-id="ddc7e-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="ddc7e-119">Tworzy token SAS konta dla obiektu blob usług, plików, tabel i kolejki, dla typów zasobów Service, Container i Object, ze wszystkimi uprawnieniami przez https oraz z określonymi datami rozpoczęcia i zakończenia</span><span class="sxs-lookup"><span data-stu-id="ddc7e-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="ddc7e-120">Ustawia definicję SAS magazynu zarządzanego przez usługę KeyVault w magazynie, a szablon uri jako utworzony powyżej token SAS, "konto" typu SAS i ważny przez 30 dni</span><span class="sxs-lookup"><span data-stu-id="ddc7e-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="ddc7e-121">pobiera rzeczywisty token dostępu z klucza tajnego KeyVault odpowiadającego definicji sas</span><span class="sxs-lookup"><span data-stu-id="ddc7e-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="ddc7e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddc7e-122">PARAMETERS</span></span>

### <span data-ttu-id="ddc7e-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ddc7e-123">-AccountName</span></span>
<span data-ttu-id="ddc7e-124">Nazwa konta magazynu zarządzanego przez magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="ddc7e-125">Polecenie cmdlet konstruuje nazwę FQDN zarządzanego konta magazynu z nazwy magazynu, obecnie wybranego środowiska i nazwy konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc7e-126">-DefaultProfile</span></span>
<span data-ttu-id="ddc7e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ddc7e-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-128">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="ddc7e-128">-Disable</span></span>
<span data-ttu-id="ddc7e-129">Wyłącza użycie definicji sas dla generowania tokenu sas.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-129">Disables the use of sas definition for generation of sas token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc7e-130">-InputObject</span></span>
<span data-ttu-id="ddc7e-131">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-131">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddc7e-132">-Name</span></span>
<span data-ttu-id="ddc7e-133">Nazwa definicji sas magazynu.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-133">Storage sas definition name.</span></span> <span data-ttu-id="ddc7e-134">Polecenie cmdlet konstruuje nazwę FQDN definicji sas magazynu z nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji sas.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="ddc7e-135">-SasType</span></span>
<span data-ttu-id="ddc7e-136">Typ SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="ddc7e-137">-Tag</span></span>
<span data-ttu-id="ddc7e-138">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ddc7e-139">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ddc7e-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ddc7e-140">-TemplateUri</span></span>
<span data-ttu-id="ddc7e-141">Storage SAS definition template uri.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="ddc7e-142">-ValidityPeriod</span></span>
<span data-ttu-id="ddc7e-143">Okres ważności używany do ustawienia czasu wygaśnięcia tokenu sas od czasu wygenerowania go</span><span class="sxs-lookup"><span data-stu-id="ddc7e-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ddc7e-144">-VaultName</span></span>
<span data-ttu-id="ddc7e-145">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-145">Vault name.</span></span>
<span data-ttu-id="ddc7e-146">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddc7e-147">-Confirm</span></span>
<span data-ttu-id="ddc7e-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc7e-149">-WhatIf</span></span>
<span data-ttu-id="ddc7e-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc7e-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc7e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc7e-152">CommonParameters</span></span>
<span data-ttu-id="ddc7e-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc7e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc7e-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddc7e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc7e-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddc7e-155">INPUTS</span></span>

### <span data-ttu-id="ddc7e-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ddc7e-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ddc7e-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddc7e-157">OUTPUTS</span></span>

### <span data-ttu-id="ddc7e-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ddc7e-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="ddc7e-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddc7e-159">NOTES</span></span>

## <span data-ttu-id="ddc7e-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddc7e-160">RELATED LINKS</span></span>

[<span data-ttu-id="ddc7e-161">Azureâ€™RM.â€™Keyâ€€Vault</span><span class="sxs-lookup"><span data-stu-id="ddc7e-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
