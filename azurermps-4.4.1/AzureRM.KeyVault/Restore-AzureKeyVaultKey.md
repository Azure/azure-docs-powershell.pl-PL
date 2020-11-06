---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553850"
---
# <span data-ttu-id="0daa6-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0daa6-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="0daa6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0daa6-102">SYNOPSIS</span></span>
<span data-ttu-id="0daa6-103">Tworzy klucz w magazynie kluczy na podstawie klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0daa6-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0daa6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0daa6-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0daa6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0daa6-105">DESCRIPTION</span></span>
<span data-ttu-id="0daa6-106">Polecenie cmdlet **Restore-AzureKeyVaultKey** tworzy klucz w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="0daa6-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="0daa6-107">Ten klucz jest repliką klucza kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz.</span><span class="sxs-lookup"><span data-stu-id="0daa6-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="0daa6-108">Jeśli w magazynie kluczy znajduje się już klucz o tej samej nazwie, zamiast zastępowania oryginalnego klucza nie jest to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0daa6-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="0daa6-109">Jeśli kopia zapasowa zawiera wiele wersji klucza, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="0daa6-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="0daa6-110">Magazyn kluczy, do którego został przywrócony klucz, może różnić się od magazynu kluczy, z którego wykonano kopię zapasową klucza.</span><span class="sxs-lookup"><span data-stu-id="0daa6-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="0daa6-111">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="0daa6-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="0daa6-112">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="0daa6-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="0daa6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0daa6-113">EXAMPLES</span></span>

### <span data-ttu-id="0daa6-114">Przykład 1: Przywracanie klucza kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="0daa6-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="0daa6-115">To polecenie przywraca klucz, w tym wszystkie wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0daa6-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="0daa6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0daa6-116">PARAMETERS</span></span>

### <span data-ttu-id="0daa6-117">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="0daa6-117">-InputFile</span></span>
<span data-ttu-id="0daa6-118">Określa plik wejściowy, który zawiera kopię zapasową klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="0daa6-118">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0daa6-119">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="0daa6-119">-VaultName</span></span>
<span data-ttu-id="0daa6-120">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz.</span><span class="sxs-lookup"><span data-stu-id="0daa6-120">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0daa6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0daa6-121">-Confirm</span></span>
<span data-ttu-id="0daa6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0daa6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0daa6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0daa6-123">-WhatIf</span></span>
<span data-ttu-id="0daa6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0daa6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0daa6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0daa6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0daa6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daa6-126">-DefaultProfile</span></span>
<span data-ttu-id="0daa6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0daa6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0daa6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daa6-128">CommonParameters</span></span>
<span data-ttu-id="0daa6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0daa6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daa6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0daa6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daa6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0daa6-131">INPUTS</span></span>

## <span data-ttu-id="0daa6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0daa6-132">OUTPUTS</span></span>

### <span data-ttu-id="0daa6-133">Microsoft. Azure. Commands. platforming. MODELES.</span><span class="sxs-lookup"><span data-stu-id="0daa6-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="0daa6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0daa6-134">NOTES</span></span>

## <span data-ttu-id="0daa6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0daa6-135">RELATED LINKS</span></span>

[<span data-ttu-id="0daa6-136">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0daa6-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="0daa6-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0daa6-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="0daa6-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0daa6-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="0daa6-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0daa6-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

