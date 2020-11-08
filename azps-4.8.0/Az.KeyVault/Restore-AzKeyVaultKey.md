---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220684"
---
# <span data-ttu-id="03559-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03559-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="03559-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03559-102">SYNOPSIS</span></span>
<span data-ttu-id="03559-103">Tworzy klucz w magazynie kluczy na podstawie klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="03559-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="03559-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03559-104">SYNTAX</span></span>

### <span data-ttu-id="03559-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03559-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03559-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03559-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03559-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03559-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03559-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03559-108">DESCRIPTION</span></span>
<span data-ttu-id="03559-109">Polecenie cmdlet **Restore-AzKeyVaultKey** tworzy klucz w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="03559-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="03559-110">Ten klucz jest repliką klucza kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz.</span><span class="sxs-lookup"><span data-stu-id="03559-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="03559-111">Jeśli w magazynie kluczy znajduje się już klucz o tej samej nazwie, zamiast zastępowania oryginalnego klucza nie jest to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03559-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="03559-112">Jeśli kopia zapasowa zawiera wiele wersji klucza, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="03559-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="03559-113">Magazyn kluczy, do którego został przywrócony klucz, może różnić się od magazynu kluczy, z którego wykonano kopię zapasową klucza.</span><span class="sxs-lookup"><span data-stu-id="03559-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="03559-114">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="03559-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="03559-115">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="03559-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="03559-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03559-116">EXAMPLES</span></span>

### <span data-ttu-id="03559-117">Przykład 1: Przywracanie klucza kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="03559-117">Example 1: Restore a backed-up key</span></span>
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

<span data-ttu-id="03559-118">To polecenie przywraca klucz, w tym wszystkie wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="03559-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="03559-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03559-119">PARAMETERS</span></span>

### <span data-ttu-id="03559-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03559-120">-DefaultProfile</span></span>
<span data-ttu-id="03559-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="03559-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03559-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="03559-122">-InputFile</span></span>
<span data-ttu-id="03559-123">Określa plik wejściowy, który zawiera kopię zapasową klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="03559-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="03559-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03559-124">-InputObject</span></span>
<span data-ttu-id="03559-125">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="03559-125">KeyVault object</span></span>

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

### <span data-ttu-id="03559-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03559-126">-ResourceId</span></span>
<span data-ttu-id="03559-127">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="03559-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="03559-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="03559-128">-VaultName</span></span>
<span data-ttu-id="03559-129">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz.</span><span class="sxs-lookup"><span data-stu-id="03559-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="03559-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03559-130">-Confirm</span></span>
<span data-ttu-id="03559-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03559-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03559-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03559-132">-WhatIf</span></span>
<span data-ttu-id="03559-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03559-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03559-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03559-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03559-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03559-135">CommonParameters</span></span>
<span data-ttu-id="03559-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03559-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03559-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03559-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03559-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03559-138">INPUTS</span></span>

### <span data-ttu-id="03559-139">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="03559-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="03559-140">System. String</span><span class="sxs-lookup"><span data-stu-id="03559-140">System.String</span></span>

## <span data-ttu-id="03559-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03559-141">OUTPUTS</span></span>

### <span data-ttu-id="03559-142">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03559-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="03559-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03559-143">NOTES</span></span>

## <span data-ttu-id="03559-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03559-144">RELATED LINKS</span></span>

[<span data-ttu-id="03559-145">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03559-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="03559-146">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03559-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="03559-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03559-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="03559-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="03559-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

