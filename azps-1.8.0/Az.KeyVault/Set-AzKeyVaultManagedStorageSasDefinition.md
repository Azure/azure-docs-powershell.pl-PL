---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 65aeede664e0817bbc3465721a14580bd897d1f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867884"
---
# <span data-ttu-id="85c92-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="85c92-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="85c92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85c92-102">SYNOPSIS</span></span>
<span data-ttu-id="85c92-103">Ustawia definicję podpisu dostępu współużytkowanego (SAS) z magazynem kluczy dla danego magazynu kluczy zarządzanego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="85c92-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="85c92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85c92-104">SYNTAX</span></span>

### <span data-ttu-id="85c92-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="85c92-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c92-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85c92-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85c92-107">Opis</span><span class="sxs-lookup"><span data-stu-id="85c92-107">DESCRIPTION</span></span>
<span data-ttu-id="85c92-108">Ustawia definicję podpisu dostępu udostępnionego (SAS) z danym magazynem kluczy zarządzanym kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="85c92-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="85c92-109">Ustawia również klucz tajny, którego można użyć w celu uzyskania tokenu SAS dla tej definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="85c92-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="85c92-110">Token SAS jest generowany przy użyciu tych parametrów i klucza aktywnego konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="85c92-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="85c92-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85c92-111">EXAMPLES</span></span>

### <span data-ttu-id="85c92-112">Przykład 1: Ustawianie definicji SAS dla typu konta i uzyskiwanie na jej podstawie bieżącego tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="85c92-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
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

<span data-ttu-id="85c92-113">Ustawia definicję SAS konta "accountsas" na koncie magazynu zarządzanego przez magazyny "mysa" w magazynie "mykv".</span><span class="sxs-lookup"><span data-stu-id="85c92-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="85c92-114">W szczególności wykonanie powyższych czynności przebiega w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="85c92-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="85c92-115">Pobiera (wstępnie istniejące) konto magazynu</span><span class="sxs-lookup"><span data-stu-id="85c92-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="85c92-116">Pobiera (wstępnie istniejący) Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="85c92-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="85c92-117">dodaje konto magazynu zarządzanego przez Magazyn kluczy do magazynu, ustawiając KEY1 jako aktywny klucz i z okresem regeneracji wy180 dni</span><span class="sxs-lookup"><span data-stu-id="85c92-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="85c92-118">Ustawia kontekst miejsca do magazynowania dla określonego konta magazynu przy użyciu funkcji KEY1</span><span class="sxs-lookup"><span data-stu-id="85c92-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="85c92-119">tworzy token SAS konta dla obiektu BLOB usług, pliku, tabeli i kolejki, dla usług typu zasobu, kontenera i obiektu, ze wszystkimi uprawnieniami, za pośrednictwem protokołu HTTPS i z określonymi datami rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="85c92-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="85c92-120">Ustawia w magazynie definicję zestawu SAS magazynu zarządzanego przez magazyn, z identyfikatorem URI szablonu jako tokenem SAS utworzonym powyżej, na koncie typu SAS (konto) i prawidłowym przez 30 dni</span><span class="sxs-lookup"><span data-stu-id="85c92-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="85c92-121">Pobiera rzeczywisty token dostępu z klucza tajnego magazynu kluczy odpowiadającego definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="85c92-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="85c92-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85c92-122">PARAMETERS</span></span>

### <span data-ttu-id="85c92-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85c92-123">-AccountName</span></span>
<span data-ttu-id="85c92-124">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="85c92-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="85c92-125">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="85c92-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="85c92-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c92-126">-DefaultProfile</span></span>
<span data-ttu-id="85c92-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="85c92-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c92-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="85c92-128">-Disable</span></span>
<span data-ttu-id="85c92-129">Wyłącza używanie definicji SAS do generowania tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="85c92-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="85c92-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85c92-130">-InputObject</span></span>
<span data-ttu-id="85c92-131">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="85c92-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="85c92-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85c92-132">-Name</span></span>
<span data-ttu-id="85c92-133">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="85c92-133">Storage sas definition name.</span></span> <span data-ttu-id="85c92-134">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="85c92-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="85c92-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="85c92-135">-SasType</span></span>
<span data-ttu-id="85c92-136">Typ SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="85c92-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="85c92-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="85c92-137">-Tag</span></span>
<span data-ttu-id="85c92-138">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="85c92-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85c92-139">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="85c92-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85c92-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="85c92-140">-TemplateUri</span></span>
<span data-ttu-id="85c92-141">Identyfikator URI szablonu definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="85c92-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="85c92-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="85c92-142">-ValidityPeriod</span></span>
<span data-ttu-id="85c92-143">Okres ważności, który zostanie wykorzystany do ustawienia czasu wygaśnięcia tokenu SAS od momentu jego wygenerowania</span><span class="sxs-lookup"><span data-stu-id="85c92-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="85c92-144">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="85c92-144">-VaultName</span></span>
<span data-ttu-id="85c92-145">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="85c92-145">Vault name.</span></span>
<span data-ttu-id="85c92-146">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="85c92-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="85c92-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85c92-147">-Confirm</span></span>
<span data-ttu-id="85c92-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c92-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c92-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c92-149">-WhatIf</span></span>
<span data-ttu-id="85c92-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c92-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c92-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85c92-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c92-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c92-152">CommonParameters</span></span>
<span data-ttu-id="85c92-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c92-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c92-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c92-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c92-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85c92-155">INPUTS</span></span>

### <span data-ttu-id="85c92-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85c92-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="85c92-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85c92-157">OUTPUTS</span></span>

### <span data-ttu-id="85c92-158">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="85c92-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="85c92-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85c92-159">NOTES</span></span>

## <span data-ttu-id="85c92-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85c92-160">RELATED LINKS</span></span>

[<span data-ttu-id="85c92-161">Azureâ € ‹ RM. â € ‹ keyâ € ‹</span><span class="sxs-lookup"><span data-stu-id="85c92-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
