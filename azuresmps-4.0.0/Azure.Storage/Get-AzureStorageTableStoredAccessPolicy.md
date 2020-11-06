---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523993"
---
# <span data-ttu-id="f69b3-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f69b3-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f69b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f69b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f69b3-103">Pobiera zasady lub zasady dostępu do tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f69b3-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="f69b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f69b3-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="f69b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f69b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f69b3-106">Polecenie cmdlet **Get-AzureStorageTableStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dotyczących tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f69b3-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="f69b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f69b3-107">EXAMPLES</span></span>

### <span data-ttu-id="f69b3-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="f69b3-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="f69b3-109">To polecenie pobiera zasady dostępu o nazwie Policy50 w tabeli magazynu o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="f69b3-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="f69b3-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="f69b3-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="f69b3-111">To polecenie pobiera wszystkie zasady dostępu w tabeli o nazwie Table02.</span><span class="sxs-lookup"><span data-stu-id="f69b3-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="f69b3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f69b3-112">PARAMETERS</span></span>

### <span data-ttu-id="f69b3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f69b3-113">-Context</span></span>
<span data-ttu-id="f69b3-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f69b3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f69b3-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f69b3-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f69b3-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="f69b3-116">-Policy</span></span>
<span data-ttu-id="f69b3-117">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="f69b3-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="f69b3-118">-Table</span><span class="sxs-lookup"><span data-stu-id="f69b3-118">-Table</span></span>
<span data-ttu-id="f69b3-119">Określa nazwę tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f69b3-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="f69b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69b3-120">CommonParameters</span></span>
<span data-ttu-id="f69b3-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69b3-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69b3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69b3-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f69b3-123">INPUTS</span></span>

## <span data-ttu-id="f69b3-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f69b3-124">OUTPUTS</span></span>

## <span data-ttu-id="f69b3-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f69b3-125">NOTES</span></span>

## <span data-ttu-id="f69b3-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f69b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="f69b3-127">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f69b3-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f69b3-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f69b3-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f69b3-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f69b3-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f69b3-130">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f69b3-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


