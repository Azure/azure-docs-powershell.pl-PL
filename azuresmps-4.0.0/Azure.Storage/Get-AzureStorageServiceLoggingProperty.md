---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524014"
---
# <span data-ttu-id="d46b6-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d46b6-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="d46b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d46b6-102">SYNOPSIS</span></span>
<span data-ttu-id="d46b6-103">Pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="d46b6-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="d46b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d46b6-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="d46b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d46b6-105">DESCRIPTION</span></span>
<span data-ttu-id="d46b6-106">Polecenie cmdlet **Get-AzureStorageServiceLoggingProperty** pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="d46b6-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="d46b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d46b6-107">EXAMPLES</span></span>

### <span data-ttu-id="d46b6-108">Przykład 1: uzyskiwanie właściwości rejestrowania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="d46b6-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="d46b6-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="d46b6-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="d46b6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d46b6-110">PARAMETERS</span></span>

### <span data-ttu-id="d46b6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d46b6-111">-Context</span></span>
<span data-ttu-id="d46b6-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d46b6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d46b6-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d46b6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d46b6-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d46b6-114">-ServiceType</span></span>
<span data-ttu-id="d46b6-115">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="d46b6-115">Specifies the storage service type.</span></span>
<span data-ttu-id="d46b6-116">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d46b6-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d46b6-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d46b6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d46b6-118">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="d46b6-118">Blob</span></span> 
- <span data-ttu-id="d46b6-119">Tworząc</span><span class="sxs-lookup"><span data-stu-id="d46b6-119">Table</span></span>
- <span data-ttu-id="d46b6-120">Wykonany</span><span class="sxs-lookup"><span data-stu-id="d46b6-120">Queue</span></span>
- <span data-ttu-id="d46b6-121">Plik</span><span class="sxs-lookup"><span data-stu-id="d46b6-121">File</span></span>

<span data-ttu-id="d46b6-122">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="d46b6-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46b6-123">CommonParameters</span></span>
<span data-ttu-id="d46b6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46b6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46b6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46b6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d46b6-126">INPUTS</span></span>

## <span data-ttu-id="d46b6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d46b6-127">OUTPUTS</span></span>

## <span data-ttu-id="d46b6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d46b6-128">NOTES</span></span>

## <span data-ttu-id="d46b6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d46b6-129">RELATED LINKS</span></span>

[<span data-ttu-id="d46b6-130">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d46b6-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d46b6-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d46b6-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


