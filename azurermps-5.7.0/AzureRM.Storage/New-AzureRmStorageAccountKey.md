---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549515"
---
# <span data-ttu-id="10329-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="10329-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="10329-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10329-102">SYNOPSIS</span></span>
<span data-ttu-id="10329-103">Generuje ponownie klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="10329-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10329-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10329-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="10329-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10329-105">DESCRIPTION</span></span>
<span data-ttu-id="10329-106">Polecenie cmdlet **New-AzureRmStorageAccountKey** generuje klucz magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="10329-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="10329-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10329-107">EXAMPLES</span></span>

### <span data-ttu-id="10329-108">Przykład 1. Regeneruj klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="10329-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="10329-109">To polecenie generuje klucz magazynu dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="10329-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="10329-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10329-110">PARAMETERS</span></span>

### <span data-ttu-id="10329-111">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="10329-111">-KeyName</span></span>
<span data-ttu-id="10329-112">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="10329-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="10329-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="10329-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10329-114">key1</span><span class="sxs-lookup"><span data-stu-id="10329-114">key1</span></span>
- <span data-ttu-id="10329-115">key2</span><span class="sxs-lookup"><span data-stu-id="10329-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10329-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10329-116">-Name</span></span>
<span data-ttu-id="10329-117">Określa nazwę konta magazynu, dla którego ma zostać ponownie wygenerowany klucz magazynu.</span><span class="sxs-lookup"><span data-stu-id="10329-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10329-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10329-118">-ResourceGroupName</span></span>
<span data-ttu-id="10329-119">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="10329-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="10329-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10329-120">CommonParameters</span></span>
<span data-ttu-id="10329-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10329-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10329-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10329-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10329-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10329-123">INPUTS</span></span>

### <span data-ttu-id="10329-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="10329-124">None</span></span>
<span data-ttu-id="10329-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="10329-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10329-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10329-126">OUTPUTS</span></span>

## <span data-ttu-id="10329-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10329-127">NOTES</span></span>

## <span data-ttu-id="10329-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10329-128">RELATED LINKS</span></span>

[<span data-ttu-id="10329-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="10329-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
