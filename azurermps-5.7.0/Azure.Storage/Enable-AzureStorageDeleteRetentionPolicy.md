---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527174"
---
# <span data-ttu-id="88c2b-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="88c2b-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="88c2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="88c2b-103">Włącz zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="88c2b-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88c2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88c2b-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="88c2b-106">Polecenie cmdlet **enable-AzureStorageDeleteRetentionPolicy** umożliwia usuwanie zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="88c2b-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="88c2b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88c2b-107">EXAMPLES</span></span>

### <span data-ttu-id="88c2b-108">Przykład 1: Włączanie zasad usuwania dotyczących przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="88c2b-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="88c2b-109">To polecenie umożliwia usuwanie zasad przechowywania dla usługi BLOB i Ustawianie usunięte dni przechowywania obiektów BLOB na wartość 3.</span><span class="sxs-lookup"><span data-stu-id="88c2b-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="88c2b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="88c2b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="88c2b-111">-Context</span></span>
<span data-ttu-id="88c2b-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="88c2b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="88c2b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88c2b-113">-PassThru</span></span>
<span data-ttu-id="88c2b-114">Wyświetlanie DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="88c2b-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="88c2b-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="88c2b-115">-RetentionDays</span></span>
<span data-ttu-id="88c2b-116">Umożliwia ustawienie liczby dni przechowywania dla DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="88c2b-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c2b-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88c2b-117">-Confirm</span></span>
<span data-ttu-id="88c2b-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c2b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c2b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c2b-119">-WhatIf</span></span>
<span data-ttu-id="88c2b-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c2b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88c2b-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88c2b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c2b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c2b-122">CommonParameters</span></span>
<span data-ttu-id="88c2b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c2b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c2b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c2b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c2b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88c2b-125">INPUTS</span></span>

### <span data-ttu-id="88c2b-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88c2b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88c2b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88c2b-127">OUTPUTS</span></span>

### <span data-ttu-id="88c2b-128">Microsoft. platformy windowsazure. Storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="88c2b-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="88c2b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88c2b-129">NOTES</span></span>

## <span data-ttu-id="88c2b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88c2b-130">RELATED LINKS</span></span>

