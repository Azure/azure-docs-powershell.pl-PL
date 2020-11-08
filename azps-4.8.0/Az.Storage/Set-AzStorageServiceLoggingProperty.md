---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222143"
---
# <span data-ttu-id="1ef65-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1ef65-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="1ef65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ef65-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef65-103">Modyfikuje rejestrowanie w usłudze Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="1ef65-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="1ef65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ef65-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ef65-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ef65-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef65-106">Polecenie cmdlet **Set-AzStorageServiceLoggingProperty** modyfikuje rejestrowanie usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="1ef65-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="1ef65-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ef65-107">EXAMPLES</span></span>

### <span data-ttu-id="1ef65-108">Przykład 1: modyfikowanie właściwości rejestrowania usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="1ef65-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="1ef65-109">To polecenie modyfikuje w wersji 1,0 rejestrowanie w magazynie obiektów blob, aby uwzględnić operacje odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="1ef65-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="1ef65-110">Rejestrowanie usługi Azure Storage Service zachowuje wpisy przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="1ef65-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="1ef65-111">Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla zmodyfikowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="1ef65-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="1ef65-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ef65-112">PARAMETERS</span></span>

### <span data-ttu-id="1ef65-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1ef65-113">-Context</span></span>
<span data-ttu-id="1ef65-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1ef65-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1ef65-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1ef65-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef65-116">-DefaultProfile</span></span>
<span data-ttu-id="1ef65-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="1ef65-118">-LoggingOperations</span></span>
<span data-ttu-id="1ef65-119">Określa tablicę operacji usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1ef65-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="1ef65-120">Usługa Azure Storage Services rejestruje operacje, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1ef65-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="1ef65-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1ef65-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ef65-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1ef65-122">None</span></span>
- <span data-ttu-id="1ef65-123">Czytał</span><span class="sxs-lookup"><span data-stu-id="1ef65-123">Read</span></span>
- <span data-ttu-id="1ef65-124">Wpisywan</span><span class="sxs-lookup"><span data-stu-id="1ef65-124">Write</span></span>
- <span data-ttu-id="1ef65-125">Usuwać</span><span class="sxs-lookup"><span data-stu-id="1ef65-125">Delete</span></span>
- <span data-ttu-id="1ef65-126">Cały</span><span class="sxs-lookup"><span data-stu-id="1ef65-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ef65-127">-PassThru</span></span>
<span data-ttu-id="1ef65-128">Wskazuje, że to polecenie cmdlet zwraca zaktualizowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="1ef65-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="1ef65-129">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="1ef65-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="1ef65-130">-RetentionDays</span></span>
<span data-ttu-id="1ef65-131">Określa liczbę dni przechowywania zarejestrowanych informacji w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1ef65-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1ef65-132">-ServiceType</span></span>
<span data-ttu-id="1ef65-133">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="1ef65-133">Specifies the storage service type.</span></span>
<span data-ttu-id="1ef65-134">To polecenie cmdlet modyfikuje właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1ef65-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1ef65-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1ef65-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ef65-136">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="1ef65-136">Blob</span></span> 
- <span data-ttu-id="1ef65-137">Tworząc</span><span class="sxs-lookup"><span data-stu-id="1ef65-137">Table</span></span>
- <span data-ttu-id="1ef65-138">Wykonany</span><span class="sxs-lookup"><span data-stu-id="1ef65-138">Queue</span></span>
- <span data-ttu-id="1ef65-139">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="1ef65-139">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-140">-Version</span><span class="sxs-lookup"><span data-stu-id="1ef65-140">-Version</span></span>
<span data-ttu-id="1ef65-141">Określa wersję rejestrowania usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1ef65-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="1ef65-142">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="1ef65-142">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef65-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef65-143">CommonParameters</span></span>
<span data-ttu-id="1ef65-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef65-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef65-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef65-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef65-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ef65-146">INPUTS</span></span>

### <span data-ttu-id="1ef65-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ef65-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1ef65-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ef65-148">OUTPUTS</span></span>

### <span data-ttu-id="1ef65-149">Microsoft. Azure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="1ef65-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="1ef65-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ef65-150">NOTES</span></span>

## <span data-ttu-id="1ef65-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ef65-151">RELATED LINKS</span></span>

[<span data-ttu-id="1ef65-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1ef65-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="1ef65-153">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ef65-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


