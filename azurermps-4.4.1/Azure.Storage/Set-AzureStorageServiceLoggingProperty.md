---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552492"
---
# <span data-ttu-id="4fe61-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4fe61-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="4fe61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fe61-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe61-103">Modyfikuje rejestrowanie w usłudze Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="4fe61-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fe61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fe61-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fe61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4fe61-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe61-106">Polecenie cmdlet **Set-AzureStorageServiceLoggingProperty** modyfikuje rejestrowanie usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="4fe61-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="4fe61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fe61-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe61-108">Przykład 1: modyfikowanie właściwości rejestrowania usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="4fe61-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="4fe61-109">To polecenie modyfikuje w wersji 1,0 rejestrowanie w magazynie obiektów blob, aby uwzględnić operacje odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="4fe61-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="4fe61-110">Rejestrowanie usługi Azure Storage Service zachowuje wpisy przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="4fe61-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="4fe61-111">Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla zmodyfikowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="4fe61-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="4fe61-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fe61-112">PARAMETERS</span></span>

### <span data-ttu-id="4fe61-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4fe61-113">-Context</span></span>
<span data-ttu-id="4fe61-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4fe61-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4fe61-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4fe61-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4fe61-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="4fe61-116">-LoggingOperations</span></span>
<span data-ttu-id="4fe61-117">Określa tablicę operacji usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4fe61-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="4fe61-118">Usługa Azure Storage Services rejestruje operacje, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4fe61-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="4fe61-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4fe61-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fe61-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4fe61-120">None</span></span>
- <span data-ttu-id="4fe61-121">Czytał</span><span class="sxs-lookup"><span data-stu-id="4fe61-121">Read</span></span>
- <span data-ttu-id="4fe61-122">Wpisywan</span><span class="sxs-lookup"><span data-stu-id="4fe61-122">Write</span></span>
- <span data-ttu-id="4fe61-123">Usuwać</span><span class="sxs-lookup"><span data-stu-id="4fe61-123">Delete</span></span>
- <span data-ttu-id="4fe61-124">Cały</span><span class="sxs-lookup"><span data-stu-id="4fe61-124">All</span></span>

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

### <span data-ttu-id="4fe61-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fe61-125">-PassThru</span></span>
<span data-ttu-id="4fe61-126">Wskazuje, że to polecenie cmdlet zwraca zaktualizowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="4fe61-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="4fe61-127">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="4fe61-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4fe61-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4fe61-128">-RetentionDays</span></span>
<span data-ttu-id="4fe61-129">Określa liczbę dni przechowywania zarejestrowanych informacji w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4fe61-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="4fe61-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4fe61-130">-ServiceType</span></span>
<span data-ttu-id="4fe61-131">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="4fe61-131">Specifies the storage service type.</span></span>
<span data-ttu-id="4fe61-132">To polecenie cmdlet modyfikuje właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4fe61-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4fe61-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4fe61-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fe61-134">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="4fe61-134">Blob</span></span> 
- <span data-ttu-id="4fe61-135">Tworząc</span><span class="sxs-lookup"><span data-stu-id="4fe61-135">Table</span></span>
- <span data-ttu-id="4fe61-136">Wykonany</span><span class="sxs-lookup"><span data-stu-id="4fe61-136">Queue</span></span>
- <span data-ttu-id="4fe61-137">Plik</span><span class="sxs-lookup"><span data-stu-id="4fe61-137">File</span></span>

<span data-ttu-id="4fe61-138">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="4fe61-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4fe61-139">-Version</span><span class="sxs-lookup"><span data-stu-id="4fe61-139">-Version</span></span>
<span data-ttu-id="4fe61-140">Określa wersję rejestrowania usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4fe61-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="4fe61-141">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fe61-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="4fe61-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe61-142">CommonParameters</span></span>
<span data-ttu-id="4fe61-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe61-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe61-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe61-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe61-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fe61-145">INPUTS</span></span>

### <span data-ttu-id="4fe61-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fe61-146">IStorageContext</span></span>

<span data-ttu-id="4fe61-147">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="4fe61-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="4fe61-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fe61-148">OUTPUTS</span></span>

### <span data-ttu-id="4fe61-149">Microsoft. platformy windowsazure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="4fe61-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="4fe61-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fe61-150">NOTES</span></span>

## <span data-ttu-id="4fe61-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fe61-151">RELATED LINKS</span></span>

[<span data-ttu-id="4fe61-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4fe61-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="4fe61-153">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fe61-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


