---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543799"
---
# <span data-ttu-id="21ca8-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="21ca8-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="21ca8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="21ca8-103">Ustawia definicję podpisu dostępu współużytkowanego (SAS) z magazynem kluczy dla danego magazynu kluczy zarządzanego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="21ca8-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ca8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21ca8-104">SYNTAX</span></span>

### <span data-ttu-id="21ca8-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="21ca8-105">Default (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21ca8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="21ca8-106">ByInputObject</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21ca8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="21ca8-108">Ustawia definicję podpisu dostępu udostępnionego (SAS) z danym magazynem kluczy zarządzanym kontem usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="21ca8-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="21ca8-109">Ustawia również klucz tajny, którego można użyć w celu uzyskania tokenu SAS dla tej definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="21ca8-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="21ca8-110">Token SAS jest generowany przy użyciu tych parametrów i klucza aktywnego konta usługi Azure Storage zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="21ca8-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="21ca8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21ca8-111">EXAMPLES</span></span>

### <span data-ttu-id="21ca8-112">Przykład 1: Ustawianie definicji SAS dla typu konta i uzyskiwanie na jej podstawie bieżącego tokenu SAS</span><span class="sxs-lookup"><span data-stu-id="21ca8-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="21ca8-113">Ustawia definicję SAS konta "accountsas" na koncie magazynu zarządzanego przez magazyny "mysa" w magazynie "mykv".</span><span class="sxs-lookup"><span data-stu-id="21ca8-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="21ca8-114">W szczególności wykonanie powyższych czynności przebiega w następujący sposób:</span><span class="sxs-lookup"><span data-stu-id="21ca8-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="21ca8-115">Pobiera (wstępnie istniejące) konto magazynu</span><span class="sxs-lookup"><span data-stu-id="21ca8-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="21ca8-116">Pobiera (wstępnie istniejący) Magazyn kluczy</span><span class="sxs-lookup"><span data-stu-id="21ca8-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="21ca8-117">dodaje konto magazynu zarządzanego przez Magazyn kluczy do magazynu, ustawiając KEY1 jako aktywny klucz i z okresem regeneracji wy180 dni</span><span class="sxs-lookup"><span data-stu-id="21ca8-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="21ca8-118">Ustawia kontekst miejsca do magazynowania dla określonego konta magazynu przy użyciu funkcji KEY1</span><span class="sxs-lookup"><span data-stu-id="21ca8-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="21ca8-119">tworzy token SAS konta dla obiektu BLOB usług, pliku, tabeli i kolejki, dla usług typu zasobu, kontenera i obiektu, ze wszystkimi uprawnieniami, za pośrednictwem protokołu HTTPS i z określonymi datami rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="21ca8-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="21ca8-120">Ustawia w magazynie definicję zestawu SAS magazynu zarządzanego przez magazyn, z identyfikatorem URI szablonu jako tokenem SAS utworzonym powyżej, na koncie typu SAS (konto) i prawidłowym przez 30 dni</span><span class="sxs-lookup"><span data-stu-id="21ca8-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="21ca8-121">Pobiera rzeczywisty token dostępu z klucza tajnego magazynu kluczy odpowiadającego definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="21ca8-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="21ca8-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21ca8-122">PARAMETERS</span></span>

### <span data-ttu-id="21ca8-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21ca8-123">-AccountName</span></span>
<span data-ttu-id="21ca8-124">Nazwa konta magazynu zarządzanego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="21ca8-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="21ca8-125">Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21ca8-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="21ca8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ca8-126">-DefaultProfile</span></span>
<span data-ttu-id="21ca8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="21ca8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ca8-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="21ca8-128">-Disable</span></span>
<span data-ttu-id="21ca8-129">Wyłącza używanie definicji SAS do generowania tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="21ca8-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="21ca8-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21ca8-130">-InputObject</span></span>
<span data-ttu-id="21ca8-131">Obiekt ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="21ca8-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="21ca8-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21ca8-132">-Name</span></span>
<span data-ttu-id="21ca8-133">Nazwa definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="21ca8-133">Storage sas definition name.</span></span> <span data-ttu-id="21ca8-134">Polecenie cmdlet tworzy nazwę FQDN definicji SAS magazynu danych na podstawie nazwy magazynu, obecnie wybranego środowiska, nazwy konta magazynu i nazwy definicji SAS.</span><span class="sxs-lookup"><span data-stu-id="21ca8-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="21ca8-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="21ca8-135">-SasType</span></span>
<span data-ttu-id="21ca8-136">Typ SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="21ca8-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="21ca8-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="21ca8-137">-Tag</span></span>
<span data-ttu-id="21ca8-138">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="21ca8-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21ca8-139">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="21ca8-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="21ca8-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="21ca8-140">-TemplateUri</span></span>
<span data-ttu-id="21ca8-141">Identyfikator URI szablonu definicji SAS magazynu.</span><span class="sxs-lookup"><span data-stu-id="21ca8-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="21ca8-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="21ca8-142">-ValidityPeriod</span></span>
<span data-ttu-id="21ca8-143">Okres ważności, który zostanie wykorzystany do ustawienia czasu wygaśnięcia tokenu SAS od momentu jego wygenerowania</span><span class="sxs-lookup"><span data-stu-id="21ca8-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="21ca8-144">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="21ca8-144">-VaultName</span></span>
<span data-ttu-id="21ca8-145">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="21ca8-145">Vault name.</span></span>
<span data-ttu-id="21ca8-146">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="21ca8-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="21ca8-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21ca8-147">-Confirm</span></span>
<span data-ttu-id="21ca8-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21ca8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ca8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ca8-149">-WhatIf</span></span>
<span data-ttu-id="21ca8-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21ca8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ca8-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21ca8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ca8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ca8-152">CommonParameters</span></span>
<span data-ttu-id="21ca8-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ca8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ca8-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ca8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ca8-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21ca8-155">INPUTS</span></span>

### <span data-ttu-id="21ca8-156">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="21ca8-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="21ca8-157">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="21ca8-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="21ca8-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21ca8-158">OUTPUTS</span></span>

### <span data-ttu-id="21ca8-159">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="21ca8-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="21ca8-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21ca8-160">NOTES</span></span>

## <span data-ttu-id="21ca8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21ca8-161">RELATED LINKS</span></span>

[<span data-ttu-id="21ca8-162">Azureâ € ‹ RM. â € ‹ keyâ € ‹</span><span class="sxs-lookup"><span data-stu-id="21ca8-162">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
