---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224274"
---
# <span data-ttu-id="9dacc-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="9dacc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9dacc-102">SYNOPSIS</span></span>
<span data-ttu-id="9dacc-103">Pobiera zarządzane klucze HSM.</span><span class="sxs-lookup"><span data-stu-id="9dacc-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="9dacc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9dacc-104">SYNTAX</span></span>

### <span data-ttu-id="9dacc-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9dacc-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="9dacc-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="9dacc-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="9dacc-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="9dacc-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="9dacc-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="9dacc-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="9dacc-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dacc-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="9dacc-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dacc-114">Opis</span><span class="sxs-lookup"><span data-stu-id="9dacc-114">DESCRIPTION</span></span>
<span data-ttu-id="9dacc-115">Polecenie cmdlet **Get-AzManagedHsmKey** pobiera klucze HSM modułu zarządzania Azure.</span><span class="sxs-lookup"><span data-stu-id="9dacc-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="9dacc-116">To polecenie cmdlet umożliwia **odwzorowanie określonego przez firmę Microsoft. Azure. Commands. DataModel. MODELES** lub lista wszystkich obiektów **pakietu** w zarządzanym pliku HSM lub w wersji.</span><span class="sxs-lookup"><span data-stu-id="9dacc-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="9dacc-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9dacc-117">EXAMPLES</span></span>

### <span data-ttu-id="9dacc-118">Przykład 1: uzyskiwanie wszystkich kluczy w zarządzanym modułu HSM</span><span class="sxs-lookup"><span data-stu-id="9dacc-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="9dacc-119">Nazwa magazynu/HSM: testmhsm Nazwa: testkey001 wersja: Identyfikator: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 włączone: prawda wygasa: nieprzed: utworzony: 10/14/2020 3:39:16 am: 10/14/2020 3:39:16 am</span><span class="sxs-lookup"><span data-stu-id="9dacc-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="9dacc-120">Nazwa magazynu/modułu HSM: testmhsm Nazwa: testkey002 wersja: Identyfikator: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 włączone: FAŁSZ wygasa: 10/14/2022 8:13:29 nie jest przed: 10/14/2020 8:13:33 am: 10/14/2020 8:14:01 AM: 10/14/2020 8:14:01 am poziom odzyskania: odzyskanie i trwałe znaczniki: Name</span><span class="sxs-lookup"><span data-stu-id="9dacc-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="9dacc-121">To polecenie pobiera wszystkie klucze z zarządzanego modułu HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="9dacc-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="9dacc-122">Przykład 2: uzyskiwanie bieżącej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="9dacc-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="9dacc-123">To polecenie pobiera bieżącą wersję klucza o nazwie testkey001 w zarządzanym HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="9dacc-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="9dacc-124">Uwaga: nazwy HSM można uzyskać za pomocą $hsm. W obszarze magazynname</span><span class="sxs-lookup"><span data-stu-id="9dacc-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="9dacc-125">Przykład 3: pobieranie wszystkich wersji klucza</span><span class="sxs-lookup"><span data-stu-id="9dacc-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="9dacc-126">To polecenie pobiera wszystkie wersje klucza o nazwie testkey001 w zarządzanym HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="9dacc-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="9dacc-127">Przykład 4: uzyskiwanie określonej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="9dacc-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="9dacc-128">To polecenie pobiera określoną wersję klucza o nazwie TestKey w zarządzanym HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="9dacc-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="9dacc-129">Po uruchomieniu tego polecenia możesz sprawdzić różne właściwości klucza, przechodząc do obiektu $Key.</span><span class="sxs-lookup"><span data-stu-id="9dacc-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="9dacc-130">Przykład 5: uzyskiwanie wszystkich kluczy, które zostały usunięte, ale nie zostały przeczyszczone dla tego zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="9dacc-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="9dacc-131">To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie zostały oczyszczone w zarządzanym programie HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="9dacc-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="9dacc-132">Przykład 6: Pobiera klucze TestKey, które zostały usunięte, ale nie zostały przeczyszczone dla tego zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="9dacc-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="9dacc-133">To polecenie pobiera klucze TestKey, które zostały wcześniej usunięte, ale nie zostały przeczyszczone w zarządzanym HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="9dacc-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="9dacc-134">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="9dacc-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="9dacc-135">Przykład 7: pobieranie wszystkich kluczy w zarządzanym składniku HSM przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="9dacc-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="9dacc-136">To polecenie pobiera wszystkie klucze z zarządzanego modułu HSM o nazwie testmhsm, które rozpoczynają się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="9dacc-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="9dacc-137">Przykład 8: Pobieranie klucza publicznego jako pliku PEM</span><span class="sxs-lookup"><span data-stu-id="9dacc-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="9dacc-138">Klucz publiczny klucza RSA można pobrać, określając `-OutFile` parametr.</span><span class="sxs-lookup"><span data-stu-id="9dacc-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="9dacc-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9dacc-139">PARAMETERS</span></span>

### <span data-ttu-id="9dacc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dacc-140">-DefaultProfile</span></span>
<span data-ttu-id="9dacc-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9dacc-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dacc-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="9dacc-142">-HsmName</span></span>
<span data-ttu-id="9dacc-143">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="9dacc-143">HSM name.</span></span> <span data-ttu-id="9dacc-144">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="9dacc-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="9dacc-145">-IncludeVersions</span></span>
<span data-ttu-id="9dacc-146">Określa, czy uwzględnić wersje klucza w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9dacc-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-147">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9dacc-147">-InputObject</span></span>
<span data-ttu-id="9dacc-148">Obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="9dacc-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9dacc-149">-InRemovedState</span></span>
<span data-ttu-id="9dacc-150">Określa, czy w wyniku mają być pokazywane uprzednio usunięte klucze.</span><span class="sxs-lookup"><span data-stu-id="9dacc-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9dacc-151">-Name</span></span>
<span data-ttu-id="9dacc-152">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="9dacc-152">Key name.</span></span>
<span data-ttu-id="9dacc-153">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="9dacc-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-154">-Plik</span><span class="sxs-lookup"><span data-stu-id="9dacc-154">-OutFile</span></span>
<span data-ttu-id="9dacc-155">Określa plik wyjściowy, dla którego to polecenie cmdlet zapisuje klucz.</span><span class="sxs-lookup"><span data-stu-id="9dacc-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="9dacc-156">Klucz publiczny jest domyślnie zapisywany w formacie PEM.</span><span class="sxs-lookup"><span data-stu-id="9dacc-156">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dacc-157">-ResourceId</span></span>
<span data-ttu-id="9dacc-158">Identyfikator zasobu HSM.</span><span class="sxs-lookup"><span data-stu-id="9dacc-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-159">-Version</span><span class="sxs-lookup"><span data-stu-id="9dacc-159">-Version</span></span>
<span data-ttu-id="9dacc-160">Wersja klucza.</span><span class="sxs-lookup"><span data-stu-id="9dacc-160">Key version.</span></span>
<span data-ttu-id="9dacc-161">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie zarządzanej nazwy modułu HSM, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="9dacc-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dacc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dacc-162">CommonParameters</span></span>
<span data-ttu-id="9dacc-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dacc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dacc-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dacc-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dacc-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dacc-165">INPUTS</span></span>

### <span data-ttu-id="9dacc-166">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9dacc-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="9dacc-167">System. String</span><span class="sxs-lookup"><span data-stu-id="9dacc-167">System.String</span></span>

## <span data-ttu-id="9dacc-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9dacc-168">OUTPUTS</span></span>

### <span data-ttu-id="9dacc-169">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9dacc-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="9dacc-170">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="9dacc-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9dacc-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="9dacc-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="9dacc-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9dacc-173">NOTES</span></span>

## <span data-ttu-id="9dacc-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9dacc-174">RELATED LINKS</span></span>

[<span data-ttu-id="9dacc-175">Dodaj-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="9dacc-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="9dacc-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="9dacc-178">Cofanie — AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="9dacc-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="9dacc-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="9dacc-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="9dacc-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)