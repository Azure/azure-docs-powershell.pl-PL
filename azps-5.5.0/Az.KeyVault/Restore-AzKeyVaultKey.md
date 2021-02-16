---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185531"
---
# <span data-ttu-id="7b80e-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b80e-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="7b80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b80e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b80e-103">Tworzy klucz w magazynie kluczy z klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7b80e-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="7b80e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7b80e-104">SYNTAX</span></span>

### <span data-ttu-id="7b80e-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7b80e-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b80e-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="7b80e-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b80e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b80e-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b80e-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b80e-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b80e-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b80e-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b80e-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b80e-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b80e-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="7b80e-111">DESCRIPTION</span></span>
<span data-ttu-id="7b80e-112">Polecenie **cmdlet Restore-AzKeyVaultKey** tworzy klucz w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="7b80e-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="7b80e-113">Ten klucz jest repliką klucza kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak klucz oryginalny.</span><span class="sxs-lookup"><span data-stu-id="7b80e-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="7b80e-114">Jeśli magazyn kluczy już ma klucz o tej samej nazwie, to polecenie cmdlet kończy się niepowodzeniem, zamiast zapełniać oryginalny klucz.</span><span class="sxs-lookup"><span data-stu-id="7b80e-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="7b80e-115">Jeśli kopia zapasowa zawiera wiele wersji klucza, wszystkie wersje są przywracane.</span><span class="sxs-lookup"><span data-stu-id="7b80e-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="7b80e-116">Magazyn kluczy, do których przywracasz klucz, może różnić się od magazynu kluczy, z których został kopii zapasowej klucza.</span><span class="sxs-lookup"><span data-stu-id="7b80e-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="7b80e-117">Jednak magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w regionie platformy Azure w tej samej lokalizacji geograficznej (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="7b80e-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="7b80e-118">Zobacz Centrum zaufania platformy Microsoft Azure (aby uzyskać informacje na temat mapowania regionów https://azure.microsoft.com/support/trust-center/) platformy Azure na obszary geograficzne).</span><span class="sxs-lookup"><span data-stu-id="7b80e-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="7b80e-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7b80e-119">EXAMPLES</span></span>

### <span data-ttu-id="7b80e-120">Przykład 1. Przywracanie klucza kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="7b80e-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="7b80e-121">To polecenie przywraca klucz, łącznie ze wszystkimi jego wersjami, z pliku kopii zapasowej o nazwie Backup.blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="7b80e-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="7b80e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b80e-122">PARAMETERS</span></span>

### <span data-ttu-id="7b80e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b80e-123">-DefaultProfile</span></span>
<span data-ttu-id="7b80e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7b80e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b80e-125">- HsmName</span><span class="sxs-lookup"><span data-stu-id="7b80e-125">-HsmName</span></span>
<span data-ttu-id="7b80e-126">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="7b80e-126">HSM name.</span></span> <span data-ttu-id="7b80e-127">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="7b80e-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-128">- HsmObject</span><span class="sxs-lookup"><span data-stu-id="7b80e-128">-HsmObject</span></span>
<span data-ttu-id="7b80e-129">Obiekt HSM</span><span class="sxs-lookup"><span data-stu-id="7b80e-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="7b80e-130">-HsmResourceId</span></span>
<span data-ttu-id="7b80e-131">Identyfikator zasobu Hsm</span><span class="sxs-lookup"><span data-stu-id="7b80e-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7b80e-132">-InputFile</span></span>
<span data-ttu-id="7b80e-133">Określa plik wejściowy zawierający kopię zapasową klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="7b80e-133">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b80e-134">-InputObject</span></span>
<span data-ttu-id="7b80e-135">Obiekt KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b80e-135">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b80e-136">-ResourceId</span></span>
<span data-ttu-id="7b80e-137">Identyfikator zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="7b80e-137">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7b80e-138">-VaultName</span></span>
<span data-ttu-id="7b80e-139">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz.</span><span class="sxs-lookup"><span data-stu-id="7b80e-139">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b80e-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b80e-140">-Confirm</span></span>
<span data-ttu-id="7b80e-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7b80e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b80e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b80e-142">-WhatIf</span></span>
<span data-ttu-id="7b80e-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b80e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b80e-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7b80e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b80e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b80e-145">CommonParameters</span></span>
<span data-ttu-id="7b80e-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b80e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b80e-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b80e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b80e-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b80e-148">INPUTS</span></span>

### <span data-ttu-id="7b80e-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7b80e-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7b80e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7b80e-150">System.String</span></span>

## <span data-ttu-id="7b80e-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b80e-151">OUTPUTS</span></span>

### <span data-ttu-id="7b80e-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b80e-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="7b80e-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7b80e-153">NOTES</span></span>

## <span data-ttu-id="7b80e-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b80e-154">RELATED LINKS</span></span>

[<span data-ttu-id="7b80e-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b80e-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="7b80e-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b80e-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="7b80e-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b80e-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="7b80e-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7b80e-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

