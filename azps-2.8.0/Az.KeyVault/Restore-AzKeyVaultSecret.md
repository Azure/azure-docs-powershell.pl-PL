---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 9fb79628b123b5d35ae5d55ba31fd07dcbd85775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705117"
---
# <span data-ttu-id="195ea-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="195ea-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="195ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="195ea-102">SYNOPSIS</span></span>
<span data-ttu-id="195ea-103">Tworzy tajemnicę w magazynie kluczy z poziomu tajnego zapasu.</span><span class="sxs-lookup"><span data-stu-id="195ea-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="195ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="195ea-104">SYNTAX</span></span>

### <span data-ttu-id="195ea-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="195ea-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="195ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="195ea-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="195ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="195ea-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195ea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="195ea-108">DESCRIPTION</span></span>
<span data-ttu-id="195ea-109">Polecenie cmdlet **Restore-AzKeyVaultSecret** tworzy klucz tajny w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="195ea-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="195ea-110">Ten klucz tajny to replika kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="195ea-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="195ea-111">Jeśli magazyn kluczy ma już klucz tajny o tej samej nazwie, nie powoduje to zastąpienia oryginalnego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="195ea-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="195ea-112">Jeśli kopia zapasowa zawiera wiele wersji klucza tajnego, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="195ea-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="195ea-113">Kluczowy magazyn, w którym można przywrócić klucz tajny, może się różnić od magazynu kluczy, na podstawie którego utworzono kopię zapasową klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="195ea-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="195ea-114">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="195ea-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="195ea-115">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="195ea-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="195ea-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="195ea-116">EXAMPLES</span></span>

### <span data-ttu-id="195ea-117">Przykład 1: Przywracanie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="195ea-117">Example 1: Restore a backed-up secret</span></span>
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

<span data-ttu-id="195ea-118">To polecenie przywraca klucz tajny wraz ze wszystkimi wersjami z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="195ea-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="195ea-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="195ea-119">PARAMETERS</span></span>

### <span data-ttu-id="195ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195ea-120">-DefaultProfile</span></span>
<span data-ttu-id="195ea-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="195ea-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="195ea-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="195ea-122">-InputFile</span></span>
<span data-ttu-id="195ea-123">Określa plik wejściowy, który zawiera kopię zapasową klucza tajnego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="195ea-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="195ea-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="195ea-124">-InputObject</span></span>
<span data-ttu-id="195ea-125">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="195ea-125">KeyVault object</span></span>

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

### <span data-ttu-id="195ea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="195ea-126">-ResourceId</span></span>
<span data-ttu-id="195ea-127">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="195ea-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="195ea-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="195ea-128">-VaultName</span></span>
<span data-ttu-id="195ea-129">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="195ea-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="195ea-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="195ea-130">-Confirm</span></span>
<span data-ttu-id="195ea-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195ea-132">-WhatIf</span></span>
<span data-ttu-id="195ea-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195ea-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="195ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195ea-135">CommonParameters</span></span>
<span data-ttu-id="195ea-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195ea-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195ea-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195ea-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="195ea-138">INPUTS</span></span>

### <span data-ttu-id="195ea-139">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="195ea-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="195ea-140">System. String</span><span class="sxs-lookup"><span data-stu-id="195ea-140">System.String</span></span>

## <span data-ttu-id="195ea-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="195ea-141">OUTPUTS</span></span>

### <span data-ttu-id="195ea-142">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="195ea-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="195ea-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="195ea-143">NOTES</span></span>

## <span data-ttu-id="195ea-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="195ea-144">RELATED LINKS</span></span>

[<span data-ttu-id="195ea-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="195ea-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="195ea-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="195ea-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="195ea-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="195ea-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="195ea-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="195ea-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

