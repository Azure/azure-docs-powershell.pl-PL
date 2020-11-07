---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: d564b9a0bf2f35240b1de75e2531858876a17475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717777"
---
# <span data-ttu-id="3bd66-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd66-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3bd66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bd66-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd66-103">Pobiera zasady lub zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd66-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bd66-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bd66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3bd66-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd66-106">Polecenie cmdlet **Get-AzureStorageTableStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd66-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3bd66-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bd66-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd66-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="3bd66-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="3bd66-109">To polecenie pobiera zasady dostępu o nazwie Policy50 w tabeli magazynu o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="3bd66-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="3bd66-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="3bd66-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="3bd66-111">To polecenie pobiera wszystkie zasady dostępu w tabeli o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="3bd66-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="3bd66-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bd66-112">PARAMETERS</span></span>

### <span data-ttu-id="3bd66-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3bd66-113">-Context</span></span>
<span data-ttu-id="3bd66-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="3bd66-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3bd66-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3bd66-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd66-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="3bd66-116">-Policy</span></span>
<span data-ttu-id="3bd66-117">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="3bd66-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd66-118">-Table</span><span class="sxs-lookup"><span data-stu-id="3bd66-118">-Table</span></span>
<span data-ttu-id="3bd66-119">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd66-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd66-120">CommonParameters</span></span>
<span data-ttu-id="3bd66-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd66-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd66-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd66-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bd66-123">INPUTS</span></span>

### <span data-ttu-id="3bd66-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bd66-124">IStorageContext</span></span>

<span data-ttu-id="3bd66-125">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="3bd66-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3bd66-126">Ciąg</span><span class="sxs-lookup"><span data-stu-id="3bd66-126">String</span></span>

<span data-ttu-id="3bd66-127">Parametr "Tabela" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="3bd66-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3bd66-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bd66-128">OUTPUTS</span></span>

### <span data-ttu-id="3bd66-129">Microsoft. platformy windowsazure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="3bd66-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="3bd66-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bd66-130">NOTES</span></span>

## <span data-ttu-id="3bd66-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bd66-131">RELATED LINKS</span></span>

[<span data-ttu-id="3bd66-132">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd66-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3bd66-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd66-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3bd66-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3bd66-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3bd66-135">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bd66-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


