---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: bd619f6c4ec9891972d23738c1f2510cba0e2272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717583"
---
# <span data-ttu-id="de563-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="de563-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="de563-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de563-102">SYNOPSIS</span></span>
<span data-ttu-id="de563-103">Tworzy tajemnicę w magazynie kluczy z poziomu tajnego zapasu.</span><span class="sxs-lookup"><span data-stu-id="de563-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de563-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de563-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de563-105">Opis</span><span class="sxs-lookup"><span data-stu-id="de563-105">DESCRIPTION</span></span>
<span data-ttu-id="de563-106">Polecenie cmdlet **Restore-AzureKeyVaultSecret** tworzy klucz tajny w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="de563-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="de563-107">Ten klucz tajny to replika kopii zapasowej w pliku wejściowym i ma taką samą nazwę jak oryginalny klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="de563-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="de563-108">Jeśli magazyn kluczy ma już klucz tajny o tej samej nazwie, nie powoduje to zastąpienia oryginalnego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="de563-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="de563-109">Jeśli kopia zapasowa zawiera wiele wersji klucza tajnego, wszystkie wersje zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="de563-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="de563-110">Kluczowy magazyn, w którym można przywrócić klucz tajny, może się różnić od magazynu kluczy, na podstawie którego utworzono kopię zapasową klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="de563-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="de563-111">Jednak Magazyn kluczy musi korzystać z tej samej subskrypcji i znajdować się w obszarze platformy Azure w tej samej geograficznej lokalizacji (na przykład w Ameryce Północnej).</span><span class="sxs-lookup"><span data-stu-id="de563-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="de563-112">Zobacz Centrum zaufania platformy Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) na potrzeby mapowania regionów usługi Azure na Geographies.</span><span class="sxs-lookup"><span data-stu-id="de563-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="de563-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de563-113">EXAMPLES</span></span>

### <span data-ttu-id="de563-114">Przykład 1: Przywracanie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="de563-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="de563-115">To polecenie przywraca klucz tajny wraz ze wszystkimi wersjami z pliku kopii zapasowej o nazwie Backup. blob do magazynu kluczy o nazwie MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="de563-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="de563-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de563-116">PARAMETERS</span></span>

### <span data-ttu-id="de563-117">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="de563-117">-InputFile</span></span>
<span data-ttu-id="de563-118">Określa plik wejściowy, który zawiera kopię zapasową klucza tajnego do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="de563-118">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="de563-119">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="de563-119">-VaultName</span></span>
<span data-ttu-id="de563-120">Określa nazwę magazynu kluczy, do którego ma zostać przywrócony klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="de563-120">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de563-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de563-121">-Confirm</span></span>
<span data-ttu-id="de563-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de563-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de563-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de563-123">-WhatIf</span></span>
<span data-ttu-id="de563-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de563-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de563-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de563-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de563-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de563-126">-DefaultProfile</span></span>
<span data-ttu-id="de563-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de563-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de563-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de563-128">CommonParameters</span></span>
<span data-ttu-id="de563-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de563-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de563-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de563-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de563-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de563-131">INPUTS</span></span>

## <span data-ttu-id="de563-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de563-132">OUTPUTS</span></span>

### <span data-ttu-id="de563-133">Microsoft. Azure. Commands. model. modeli. Secret</span><span class="sxs-lookup"><span data-stu-id="de563-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="de563-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de563-134">NOTES</span></span>

## <span data-ttu-id="de563-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de563-135">RELATED LINKS</span></span>

[<span data-ttu-id="de563-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="de563-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="de563-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="de563-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="de563-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="de563-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="de563-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="de563-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

