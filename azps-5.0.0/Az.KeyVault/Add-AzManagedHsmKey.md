---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234703"
---
# <span data-ttu-id="0d7fc-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d7fc-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="0d7fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7fc-103">Tworzy klucz w zarządzanym pliku HSM lub importuje klucz do zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="0d7fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d7fc-104">SYNTAX</span></span>

### <span data-ttu-id="0d7fc-105">InteractiveCreate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d7fc-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="0d7fc-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="0d7fc-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="0d7fc-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="0d7fc-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7fc-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="0d7fc-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d7fc-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0d7fc-111">DESCRIPTION</span></span>
<span data-ttu-id="0d7fc-112">Polecenie cmdlet **Add-AzManagedHsmKey** tworzy klucz w zarządzanym modułu HSM w zarządzanym systemie Azure lub importuje klucz do zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="0d7fc-113">Za pomocą tego polecenia cmdlet można dodawać klucze przy użyciu dowolnej z poniższych metod:</span><span class="sxs-lookup"><span data-stu-id="0d7fc-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="0d7fc-114">Tworzenie klucza z domyślnymi atrybutami klucza</span><span class="sxs-lookup"><span data-stu-id="0d7fc-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="0d7fc-115">Tworzenie klucza z podanymi atrybutami klucza</span><span class="sxs-lookup"><span data-stu-id="0d7fc-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="0d7fc-116">Importowanie klucza z pliku PFX na komputerze.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="0d7fc-117">W przypadku dowolnej z tych operacji możesz podać atrybuty klucza lub zaakceptować ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="0d7fc-118">W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w zarządzanym programie HSM, oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="0d7fc-119">Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="0d7fc-120">Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach i hasłach](http://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w zarządzanym pakiecie HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="0d7fc-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d7fc-121">EXAMPLES</span></span>

### <span data-ttu-id="0d7fc-122">Przykład 1. Tworzenie klucza modułu RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="0d7fc-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="0d7fc-123">To polecenie tworzy klucz modułu RSA o nazwie TestKey w zarządzanym pliku HSM TestKey o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="0d7fc-124">Przykład 2: Tworzenie klucza we-HSM</span><span class="sxs-lookup"><span data-stu-id="0d7fc-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="0d7fc-125">To polecenie tworzy klucz EC-HSM o nazwie TestKey przy użyciu krzywej P-256 w zarządzanym TestKey modułu HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="0d7fc-126">Przykład 3: Tworzenie klucza modułu HSM z wartościami niedomyślnymi</span><span class="sxs-lookup"><span data-stu-id="0d7fc-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
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

<span data-ttu-id="0d7fc-127">Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="0d7fc-128">Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="0d7fc-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0d7fc-129">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="0d7fc-130">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="0d7fc-131">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0d7fc-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0d7fc-132">Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="0d7fc-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0d7fc-133">Ten obiekt określa bieżący czas UTC.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-133">That object specifies current UTC time.</span></span> <span data-ttu-id="0d7fc-134">Polecenie zapisuje tę datę w zmiennej $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="0d7fc-135">Ostatnie polecenie tworzy klucz o nazwie TestKey, który jest kluczem HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="0d7fc-136">W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="0d7fc-137">Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="0d7fc-138">Nowy klucz jest wyłączony.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-138">The new key is disabled.</span></span> <span data-ttu-id="0d7fc-139">Możesz ją włączyć za pomocą polecenia cmdlet **Update-AzManagedHsmKey** .</span><span class="sxs-lookup"><span data-stu-id="0d7fc-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="0d7fc-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d7fc-140">PARAMETERS</span></span>

### <span data-ttu-id="0d7fc-141">-Zakrętname</span><span class="sxs-lookup"><span data-stu-id="0d7fc-141">-CurveName</span></span>
<span data-ttu-id="0d7fc-142">Określa nazwę krzywej kryptografii krzywej eliptycznej, która jest prawidłowa, gdy właściwość KeyType ma wartość EC.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="0d7fc-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7fc-143">-DefaultProfile</span></span>
<span data-ttu-id="0d7fc-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d7fc-145">-Disable</span><span class="sxs-lookup"><span data-stu-id="0d7fc-145">-Disable</span></span>
<span data-ttu-id="0d7fc-146">Wskazuje, że dodawany klawisz jest ustawiony na początkowy stan wyłączony.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="0d7fc-147">Każda próba użycia tego klawisza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="0d7fc-148">Tego parametru należy użyć, jeśli wstępnie załadowano klucze, które mają być później włączone.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="0d7fc-149">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="0d7fc-149">-Expires</span></span>
<span data-ttu-id="0d7fc-150">Określa czas wygaśnięcia klucza w formacie UTC.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="0d7fc-151">Jeśli nie określono tego parametru, klucz nie wygasa.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0d7fc-152">-HsmName</span></span>
<span data-ttu-id="0d7fc-153">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-153">HSM name.</span></span> <span data-ttu-id="0d7fc-154">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-155">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d7fc-155">-InputObject</span></span>
<span data-ttu-id="0d7fc-156">Obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="0d7fc-157">-KeyFilePassword</span></span>
<span data-ttu-id="0d7fc-158">Hasło do pliku lokalnego zawierającego kluczowy materiał do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-159">-FilePath</span><span class="sxs-lookup"><span data-stu-id="0d7fc-159">-KeyFilePath</span></span>
<span data-ttu-id="0d7fc-160">Ścieżka do pliku lokalnego zawierającego kluczowy materiał do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="0d7fc-161">-KeyOps</span></span>
<span data-ttu-id="0d7fc-162">Operacje, które można wykonać przy użyciu klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="0d7fc-163">W przypadku nieobecności można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0d7fc-164">-KeyType</span></span>
<span data-ttu-id="0d7fc-165">Określa typ klucza dla tego klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-166">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d7fc-166">-Name</span></span>
<span data-ttu-id="0d7fc-167">Nazwa klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-167">Key name.</span></span>
<span data-ttu-id="0d7fc-168">Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0d7fc-169">-NotBefore</span></span>
<span data-ttu-id="0d7fc-170">Czas UTC, po upływie którego nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="0d7fc-171">Jeśli nie określono tego, nie ma ograniczeń.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d7fc-172">-ResourceId</span></span>
<span data-ttu-id="0d7fc-173">Identyfikator zasobu HSM.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-174">-Size</span><span class="sxs-lookup"><span data-stu-id="0d7fc-174">-Size</span></span>
<span data-ttu-id="0d7fc-175">Rozmiar klucza RSA w bitach.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-175">RSA key size, in bits.</span></span>
<span data-ttu-id="0d7fc-176">Jeśli nie zostanie określona, usługa będzie dostarczać bezpieczne ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d7fc-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d7fc-177">-Tag</span></span>
<span data-ttu-id="0d7fc-178">Obiekt Hashtable reprezentujący Tagi kluczowe.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-178">A hashtable representing key tags.</span></span>

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

### <span data-ttu-id="0d7fc-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d7fc-179">-Confirm</span></span>
<span data-ttu-id="0d7fc-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7fc-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7fc-181">-WhatIf</span></span>
<span data-ttu-id="0d7fc-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7fc-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7fc-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7fc-184">CommonParameters</span></span>
<span data-ttu-id="0d7fc-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d7fc-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7fc-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d7fc-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7fc-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d7fc-187">INPUTS</span></span>

### <span data-ttu-id="0d7fc-188">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0d7fc-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="0d7fc-189">System. String</span><span class="sxs-lookup"><span data-stu-id="0d7fc-189">System.String</span></span>

## <span data-ttu-id="0d7fc-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d7fc-190">OUTPUTS</span></span>

### <span data-ttu-id="0d7fc-191">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="0d7fc-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="0d7fc-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d7fc-192">NOTES</span></span>

## <span data-ttu-id="0d7fc-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d7fc-193">RELATED LINKS</span></span>

[<span data-ttu-id="0d7fc-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d7fc-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="0d7fc-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d7fc-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="0d7fc-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d7fc-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="0d7fc-197">Cofanie — AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0d7fc-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="0d7fc-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d7fc-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="0d7fc-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d7fc-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
