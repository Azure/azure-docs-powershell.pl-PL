---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234671"
---
# <span data-ttu-id="360c3-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="360c3-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="360c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="360c3-102">SYNOPSIS</span></span>
<span data-ttu-id="360c3-103">Tworzy klucz w zarządzanym pliku HSM z poziomu klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="360c3-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="360c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="360c3-104">SYNTAX</span></span>

### <span data-ttu-id="360c3-105">ByHsmName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="360c3-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="360c3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="360c3-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="360c3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="360c3-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360c3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="360c3-108">DESCRIPTION</span></span>
<span data-ttu-id="360c3-109">Polecenie cmdlet **Restore-AzManagedHsmKey** tworzy klucz w określonym zarządzanym składniku HSM.</span><span class="sxs-lookup"><span data-stu-id="360c3-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="360c3-110">Ten klucz jest repliką klucza kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz.</span><span class="sxs-lookup"><span data-stu-id="360c3-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="360c3-111">Jeśli zarządzany element HSM ma już klucz o tej samej nazwie, zamiast zastępowania oryginalnego klucza nie zastąpi to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="360c3-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="360c3-112">Jeśli kopia zapasowa zawiera wiele wersji klucza, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="360c3-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="360c3-113">Zarządzany program HSM, do którego został przywrócony klucz, może być różny od zarządzanego modułu HSM, z którego wykonano kopię zapasową klucza.</span><span class="sxs-lookup"><span data-stu-id="360c3-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="360c3-114">Jednak zarządzany składnik HSM musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="360c3-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="360c3-115">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="360c3-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="360c3-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="360c3-116">EXAMPLES</span></span>

### <span data-ttu-id="360c3-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="360c3-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="360c3-118">To polecenie przywraca klucz, w tym wszystkie wersje, z pliku kopii zapasowej o nazwie Backup. blob do zarządzanego modułu HSM o nazwie testmhsm.</span><span class="sxs-lookup"><span data-stu-id="360c3-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="360c3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="360c3-119">PARAMETERS</span></span>

### <span data-ttu-id="360c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360c3-120">-DefaultProfile</span></span>
<span data-ttu-id="360c3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="360c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="360c3-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="360c3-122">-HsmName</span></span>
<span data-ttu-id="360c3-123">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="360c3-123">HSM name.</span></span> <span data-ttu-id="360c3-124">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="360c3-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360c3-125">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="360c3-125">-InputFile</span></span>
<span data-ttu-id="360c3-126">Plik wejściowy.</span><span class="sxs-lookup"><span data-stu-id="360c3-126">Input file.</span></span>
<span data-ttu-id="360c3-127">Plik wejściowy zawierający obiekt BLOB z kopią zapasową</span><span class="sxs-lookup"><span data-stu-id="360c3-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="360c3-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="360c3-128">-InputObject</span></span>
<span data-ttu-id="360c3-129">Obiekt HSM</span><span class="sxs-lookup"><span data-stu-id="360c3-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="360c3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="360c3-130">-ResourceId</span></span>
<span data-ttu-id="360c3-131">Identyfikator zasobu HSM</span><span class="sxs-lookup"><span data-stu-id="360c3-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="360c3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="360c3-132">-Confirm</span></span>
<span data-ttu-id="360c3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="360c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360c3-134">-WhatIf</span></span>
<span data-ttu-id="360c3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="360c3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360c3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="360c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360c3-137">CommonParameters</span></span>
<span data-ttu-id="360c3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360c3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="360c3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360c3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="360c3-140">INPUTS</span></span>

### <span data-ttu-id="360c3-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="360c3-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="360c3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="360c3-142">System.String</span></span>

## <span data-ttu-id="360c3-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="360c3-143">OUTPUTS</span></span>

### <span data-ttu-id="360c3-144">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="360c3-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="360c3-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="360c3-145">NOTES</span></span>

## <span data-ttu-id="360c3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="360c3-146">RELATED LINKS</span></span>

[<span data-ttu-id="360c3-147">Dodaj-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="360c3-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="360c3-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="360c3-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="360c3-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="360c3-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="360c3-150">Cofanie — AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="360c3-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="360c3-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="360c3-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="360c3-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="360c3-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)