---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893030"
---
# <span data-ttu-id="1b944-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1b944-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="1b944-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b944-102">SYNOPSIS</span></span>
<span data-ttu-id="1b944-103">Tworzy tajemnicę w magazynie kluczy z poziomu tajnego zapasu.</span><span class="sxs-lookup"><span data-stu-id="1b944-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="1b944-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b944-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b944-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b944-105">DESCRIPTION</span></span>
<span data-ttu-id="1b944-106">Polecenie cmdlet **Restore-AzKeyVaultSecret** tworzy klucz tajny w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1b944-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="1b944-107">Ten klucz tajny to replika kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="1b944-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="1b944-108">Jeśli magazyn kluczy ma już klucz tajny o tej samej nazwie, nie powoduje to zastąpienia oryginalnego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="1b944-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="1b944-109">Jeśli kopia zapasowa zawiera wiele wersji klucza tajnego, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="1b944-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="1b944-110">Kluczowy magazyn, w którym można przywrócić klucz tajny, może się różnić od magazynu kluczy, na podstawie którego utworzono kopię zapasową klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="1b944-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="1b944-111">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="1b944-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="1b944-112">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="1b944-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="1b944-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b944-113">EXAMPLES</span></span>

### <span data-ttu-id="1b944-114">Przykład 1: Przywracanie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="1b944-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="1b944-115">To polecenie przywraca klucz tajny wraz ze wszystkimi wersjami z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="1b944-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="1b944-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b944-116">PARAMETERS</span></span>

### <span data-ttu-id="1b944-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b944-117">-DefaultProfile</span></span>
<span data-ttu-id="1b944-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1b944-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b944-119">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="1b944-119">-InputFile</span></span>
<span data-ttu-id="1b944-120">Określa plik wejściowy, który zawiera kopię zapasową klucza tajnego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="1b944-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="1b944-121">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1b944-121">-VaultName</span></span>
<span data-ttu-id="1b944-122">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="1b944-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="1b944-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b944-123">-Confirm</span></span>
<span data-ttu-id="1b944-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b944-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b944-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b944-125">-WhatIf</span></span>
<span data-ttu-id="1b944-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b944-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b944-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b944-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b944-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b944-128">CommonParameters</span></span>
<span data-ttu-id="1b944-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b944-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b944-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b944-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b944-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b944-131">INPUTS</span></span>

### <span data-ttu-id="1b944-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1b944-132">None</span></span>
<span data-ttu-id="1b944-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1b944-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b944-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b944-134">OUTPUTS</span></span>

### <span data-ttu-id="1b944-135">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="1b944-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="1b944-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b944-136">NOTES</span></span>

## <span data-ttu-id="1b944-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b944-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b944-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1b944-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="1b944-139">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1b944-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="1b944-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1b944-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="1b944-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1b944-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

