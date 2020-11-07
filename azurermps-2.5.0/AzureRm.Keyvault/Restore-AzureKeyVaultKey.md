---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7bad1311d463b8372d07a33c549682a2cade4041
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897353"
---
# <span data-ttu-id="575da-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575da-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="575da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="575da-102">SYNOPSIS</span></span>
<span data-ttu-id="575da-103">Tworzy klucz w magazynie kluczy na podstawie klucza kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="575da-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="575da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="575da-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="575da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="575da-105">DESCRIPTION</span></span>
<span data-ttu-id="575da-106">Polecenie cmdlet **Restore-AzureKeyVaultKey** tworzy klucz w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="575da-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="575da-107">Ten klucz jest repliką klucza kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz.</span><span class="sxs-lookup"><span data-stu-id="575da-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="575da-108">Jeśli w magazynie kluczy znajduje się już klucz o tej samej nazwie, zamiast zastępowania oryginalnego klucza nie jest to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575da-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="575da-109">Jeśli kopia zapasowa zawiera wiele wersji klucza, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="575da-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="575da-110">Magazyn kluczy, do którego został przywrócony klucz, może różnić się od magazynu kluczy, z którego wykonano kopię zapasową klucza.</span><span class="sxs-lookup"><span data-stu-id="575da-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="575da-111">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="575da-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="575da-112">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="575da-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="575da-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="575da-113">EXAMPLES</span></span>

### <span data-ttu-id="575da-114">Przykład 1: Przywracanie klucza kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="575da-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="575da-115">To polecenie przywraca klucz, w tym wszystkie wersje, z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="575da-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="575da-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="575da-116">PARAMETERS</span></span>

### <span data-ttu-id="575da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575da-117">-DefaultProfile</span></span>
<span data-ttu-id="575da-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="575da-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575da-119">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="575da-119">-InputFile</span></span>
<span data-ttu-id="575da-120">Określa plik wejściowy, który zawiera kopię zapasową klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="575da-120">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575da-121">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="575da-121">-VaultName</span></span>
<span data-ttu-id="575da-122">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz.</span><span class="sxs-lookup"><span data-stu-id="575da-122">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="575da-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="575da-123">-Confirm</span></span>
<span data-ttu-id="575da-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575da-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575da-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575da-125">-WhatIf</span></span>
<span data-ttu-id="575da-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575da-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575da-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="575da-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575da-128">CommonParameters</span></span>
<span data-ttu-id="575da-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575da-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575da-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="575da-131">INPUTS</span></span>

## <span data-ttu-id="575da-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="575da-132">OUTPUTS</span></span>

### <span data-ttu-id="575da-133">Microsoft. Azure. Commands. platforming. MODELES.</span><span class="sxs-lookup"><span data-stu-id="575da-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="575da-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="575da-134">NOTES</span></span>

## <span data-ttu-id="575da-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="575da-135">RELATED LINKS</span></span>

[<span data-ttu-id="575da-136">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575da-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="575da-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575da-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="575da-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575da-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="575da-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="575da-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

