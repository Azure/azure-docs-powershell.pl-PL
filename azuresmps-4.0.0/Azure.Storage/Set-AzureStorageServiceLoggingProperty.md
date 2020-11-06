---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524129"
---
# <span data-ttu-id="a924d-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a924d-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="a924d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a924d-102">SYNOPSIS</span></span>
<span data-ttu-id="a924d-103">Modyfikuje rejestrowanie w usłudze Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="a924d-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="a924d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a924d-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="a924d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a924d-105">DESCRIPTION</span></span>
<span data-ttu-id="a924d-106">Polecenie cmdlet **Set-AzureStorageServiceLoggingProperty** modyfikuje rejestrowanie usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="a924d-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="a924d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a924d-107">EXAMPLES</span></span>

### <span data-ttu-id="a924d-108">Przykład 1: modyfikowanie właściwości rejestrowania usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="a924d-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="a924d-109">To polecenie modyfikuje w wersji 1,0 rejestrowanie w magazynie obiektów blob, aby uwzględnić operacje odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="a924d-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="a924d-110">Rejestrowanie usługi Azure Storage Service zachowuje wpisy przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="a924d-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="a924d-111">Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla zmodyfikowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="a924d-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="a924d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a924d-112">PARAMETERS</span></span>

### <span data-ttu-id="a924d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a924d-113">-Context</span></span>
<span data-ttu-id="a924d-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a924d-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a924d-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a924d-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a924d-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="a924d-116">-LoggingOperations</span></span>
<span data-ttu-id="a924d-117">Określa tablicę operacji usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a924d-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="a924d-118">Usługa Azure Storage Services rejestruje operacje, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a924d-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="a924d-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a924d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a924d-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a924d-120">None</span></span>
- <span data-ttu-id="a924d-121">Czytał</span><span class="sxs-lookup"><span data-stu-id="a924d-121">Read</span></span>
- <span data-ttu-id="a924d-122">Wpisywan</span><span class="sxs-lookup"><span data-stu-id="a924d-122">Write</span></span>
- <span data-ttu-id="a924d-123">Usuwać</span><span class="sxs-lookup"><span data-stu-id="a924d-123">Delete</span></span>
- <span data-ttu-id="a924d-124">Cały</span><span class="sxs-lookup"><span data-stu-id="a924d-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a924d-125">-PassThru</span></span>
<span data-ttu-id="a924d-126">Wskazuje, że to polecenie cmdlet zwraca zaktualizowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="a924d-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="a924d-127">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a924d-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924d-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="a924d-128">-RetentionDays</span></span>
<span data-ttu-id="a924d-129">Określa liczbę dni przechowywania zarejestrowanych informacji w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a924d-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924d-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a924d-130">-ServiceType</span></span>
<span data-ttu-id="a924d-131">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="a924d-131">Specifies the storage service type.</span></span>
<span data-ttu-id="a924d-132">To polecenie cmdlet modyfikuje właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a924d-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="a924d-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a924d-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a924d-134">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="a924d-134">Blob</span></span> 
- <span data-ttu-id="a924d-135">Tworząc</span><span class="sxs-lookup"><span data-stu-id="a924d-135">Table</span></span>
- <span data-ttu-id="a924d-136">Wykonany</span><span class="sxs-lookup"><span data-stu-id="a924d-136">Queue</span></span>
- <span data-ttu-id="a924d-137">Plik</span><span class="sxs-lookup"><span data-stu-id="a924d-137">File</span></span>

<span data-ttu-id="a924d-138">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="a924d-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="a924d-139">-Version</span><span class="sxs-lookup"><span data-stu-id="a924d-139">-Version</span></span>
<span data-ttu-id="a924d-140">Określa wersję rejestrowania usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a924d-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="a924d-141">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="a924d-141">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a924d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a924d-142">CommonParameters</span></span>
<span data-ttu-id="a924d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a924d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a924d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a924d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a924d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a924d-145">INPUTS</span></span>

## <span data-ttu-id="a924d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a924d-146">OUTPUTS</span></span>

## <span data-ttu-id="a924d-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a924d-147">NOTES</span></span>

## <span data-ttu-id="a924d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a924d-148">RELATED LINKS</span></span>

[<span data-ttu-id="a924d-149">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a924d-149">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="a924d-150">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a924d-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


