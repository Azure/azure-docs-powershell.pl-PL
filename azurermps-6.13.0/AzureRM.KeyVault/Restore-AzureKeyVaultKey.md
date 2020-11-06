---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 70c56aaee4bf6547ad932965a190d3ecb2d93f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527929"
---
# <span data-ttu-id="a842f-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a842f-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="a842f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a842f-102">SYNOPSIS</span></span>
<span data-ttu-id="a842f-103">Tworzy klucz w magazynie kluczy na podstawie klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="a842f-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a842f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a842f-104">SYNTAX</span></span>

### <span data-ttu-id="a842f-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a842f-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a842f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a842f-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a842f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a842f-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultKey [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a842f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a842f-108">DESCRIPTION</span></span>
<span data-ttu-id="a842f-109">Polecenie cmdlet **Restore-AzureKeyVaultKey** tworzy klucz w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="a842f-109">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="a842f-110">Ten klucz jest repliką klucza kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz.</span><span class="sxs-lookup"><span data-stu-id="a842f-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="a842f-111">Jeśli w magazynie kluczy znajduje się już klucz o tej samej nazwie, zamiast zastępowania oryginalnego klucza nie jest to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a842f-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="a842f-112">Jeśli kopia zapasowa zawiera wiele wersji klucza, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="a842f-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="a842f-113">Magazyn kluczy, do którego został przywrócony klucz, może różnić się od magazynu kluczy, z którego wykonano kopię zapasową klucza.</span><span class="sxs-lookup"><span data-stu-id="a842f-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="a842f-114">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="a842f-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a842f-115">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="a842f-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a842f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a842f-116">EXAMPLES</span></span>

### <span data-ttu-id="a842f-117">Przykład 1: Przywracanie klucza kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="a842f-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="a842f-118">To polecenie przywraca klucz, w tym wszystkie wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a842f-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="a842f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a842f-119">PARAMETERS</span></span>

### <span data-ttu-id="a842f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a842f-120">-DefaultProfile</span></span>
<span data-ttu-id="a842f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a842f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a842f-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="a842f-122">-InputFile</span></span>
<span data-ttu-id="a842f-123">Określa plik wejściowy, który zawiera kopię zapasową klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="a842f-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="a842f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a842f-124">-InputObject</span></span>
<span data-ttu-id="a842f-125">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="a842f-125">KeyVault object</span></span>

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

### <span data-ttu-id="a842f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a842f-126">-ResourceId</span></span>
<span data-ttu-id="a842f-127">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="a842f-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="a842f-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="a842f-128">-VaultName</span></span>
<span data-ttu-id="a842f-129">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz.</span><span class="sxs-lookup"><span data-stu-id="a842f-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="a842f-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a842f-130">-Confirm</span></span>
<span data-ttu-id="a842f-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a842f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a842f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a842f-132">-WhatIf</span></span>
<span data-ttu-id="a842f-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a842f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a842f-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a842f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a842f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a842f-135">CommonParameters</span></span>
<span data-ttu-id="a842f-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a842f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a842f-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a842f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a842f-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a842f-138">INPUTS</span></span>

### <span data-ttu-id="a842f-139">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a842f-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="a842f-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a842f-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a842f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a842f-141">System.String</span></span>

## <span data-ttu-id="a842f-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a842f-142">OUTPUTS</span></span>

### <span data-ttu-id="a842f-143">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a842f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="a842f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a842f-144">NOTES</span></span>

## <span data-ttu-id="a842f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a842f-145">RELATED LINKS</span></span>

[<span data-ttu-id="a842f-146">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a842f-146">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="a842f-147">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a842f-147">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="a842f-148">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a842f-148">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="a842f-149">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a842f-149">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

