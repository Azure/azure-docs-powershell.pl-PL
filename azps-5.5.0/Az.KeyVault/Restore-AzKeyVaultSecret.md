---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185523"
---
# <span data-ttu-id="257d5-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="257d5-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="257d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="257d5-102">SYNOPSIS</span></span>
<span data-ttu-id="257d5-103">Tworzy klucz tajny w magazynie kluczy z kopii zapasowej tajnej.</span><span class="sxs-lookup"><span data-stu-id="257d5-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="257d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="257d5-104">SYNTAX</span></span>

### <span data-ttu-id="257d5-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="257d5-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257d5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="257d5-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257d5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="257d5-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257d5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="257d5-108">DESCRIPTION</span></span>
<span data-ttu-id="257d5-109">Polecenie **cmdlet Restore-AzKeyVaultSecret** tworzy klucz tajny w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="257d5-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="257d5-110">Ta tajemnica jest repliką kopii zapasowej tajnej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="257d5-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="257d5-111">Jeśli magazyn kluczy ma już klucz tajny o tej samej nazwie, to polecenie cmdlet kończy się niepowodzeniem, zamiast zapełniać pierwotną tajemnicę.</span><span class="sxs-lookup"><span data-stu-id="257d5-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="257d5-112">Jeśli kopia zapasowa zawiera wiele wersji tajnych, wszystkie wersje są przywracane.</span><span class="sxs-lookup"><span data-stu-id="257d5-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="257d5-113">Magazyn kluczy, z których przywracany jest klucz tajny, może różnić się od magazynu kluczy, z których jest tworzyć kopię zapasową klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="257d5-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="257d5-114">Jednak magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w regionie platformy Azure w tej samej lokalizacji geograficznej (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="257d5-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="257d5-115">Zobacz Centrum zaufania platformy Microsoft Azure (aby uzyskać informacje na temat mapowania regionów https://azure.microsoft.com/support/trust-center/) platformy Azure na obszary geograficzne).</span><span class="sxs-lookup"><span data-stu-id="257d5-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="257d5-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="257d5-116">EXAMPLES</span></span>

### <span data-ttu-id="257d5-117">Przykład 1. Przywracanie kopii zapasowej tajnej</span><span class="sxs-lookup"><span data-stu-id="257d5-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="257d5-118">To polecenie przywraca klucz tajny, w tym wszystkie jego wersje, z pliku kopii zapasowej o nazwie Backup.blob do magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="257d5-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="257d5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="257d5-119">PARAMETERS</span></span>

### <span data-ttu-id="257d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257d5-120">-DefaultProfile</span></span>
<span data-ttu-id="257d5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="257d5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="257d5-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="257d5-122">-InputFile</span></span>
<span data-ttu-id="257d5-123">Określa plik wejściowy zawierający kopię zapasową informacji tajnej do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="257d5-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="257d5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="257d5-124">-InputObject</span></span>
<span data-ttu-id="257d5-125">Obiekt KeyVault</span><span class="sxs-lookup"><span data-stu-id="257d5-125">KeyVault object</span></span>

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

### <span data-ttu-id="257d5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="257d5-126">-ResourceId</span></span>
<span data-ttu-id="257d5-127">Identyfikator zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="257d5-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="257d5-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="257d5-128">-VaultName</span></span>
<span data-ttu-id="257d5-129">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="257d5-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="257d5-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="257d5-130">-Confirm</span></span>
<span data-ttu-id="257d5-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="257d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257d5-132">-WhatIf</span></span>
<span data-ttu-id="257d5-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="257d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257d5-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="257d5-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257d5-135">CommonParameters</span></span>
<span data-ttu-id="257d5-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257d5-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="257d5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257d5-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="257d5-138">INPUTS</span></span>

### <span data-ttu-id="257d5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="257d5-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="257d5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="257d5-140">System.String</span></span>

## <span data-ttu-id="257d5-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="257d5-141">OUTPUTS</span></span>

### <span data-ttu-id="257d5-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="257d5-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="257d5-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="257d5-143">NOTES</span></span>

## <span data-ttu-id="257d5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="257d5-144">RELATED LINKS</span></span>

[<span data-ttu-id="257d5-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="257d5-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="257d5-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="257d5-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="257d5-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="257d5-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="257d5-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="257d5-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

