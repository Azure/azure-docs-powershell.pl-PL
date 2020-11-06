---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523845"
---
# <span data-ttu-id="a8ac9-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a8ac9-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="a8ac9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ac9-103">Tworzy tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-103">Creates a storage table.</span></span>

## <span data-ttu-id="a8ac9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8ac9-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a8ac9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ac9-106">Polecenie cmdlet **New-AzureStorageTable** tworzy tabelę magazynu skojarzoną z kontem magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a8ac9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="a8ac9-108">Przykład 1. Tworzenie tabeli magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a8ac9-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="a8ac9-109">To polecenie tworzy tabelę magazynu o nazwie tableabc.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="a8ac9-110">Przykład 2: Tworzenie wielu tabel magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a8ac9-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="a8ac9-111">To polecenie powoduje utworzenie wielu tabel.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-111">This command creates multiple tables.</span></span>
<span data-ttu-id="a8ac9-112">Używa metody **Split** klasy **String** programu .NET, a następnie przekazuje imiona i nazwiska w potoku.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a8ac9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8ac9-113">PARAMETERS</span></span>

### <span data-ttu-id="a8ac9-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a8ac9-114">-Context</span></span>
<span data-ttu-id="a8ac9-115">Określa kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-115">Specifies the storage context.</span></span>
<span data-ttu-id="a8ac9-116">Aby ją utworzyć, możesz użyć New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a8ac9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8ac9-117">-Name</span></span>
<span data-ttu-id="a8ac9-118">Określa nazwę nowej tabeli.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ac9-119">CommonParameters</span></span>
<span data-ttu-id="a8ac9-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ac9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ac9-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ac9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ac9-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8ac9-122">INPUTS</span></span>

## <span data-ttu-id="a8ac9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8ac9-123">OUTPUTS</span></span>

## <span data-ttu-id="a8ac9-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8ac9-124">NOTES</span></span>

## <span data-ttu-id="a8ac9-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8ac9-125">RELATED LINKS</span></span>

[<span data-ttu-id="a8ac9-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a8ac9-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="a8ac9-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a8ac9-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


