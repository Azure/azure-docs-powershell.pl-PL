---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716652"
---
# <span data-ttu-id="f75ed-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f75ed-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f75ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f75ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f75ed-103">Wyłącz zasadę usuwania zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="f75ed-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f75ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f75ed-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f75ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f75ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f75ed-106">Polecenie cmdlet **disable-AzureStorageDeleteRetentionPolicy** wyłącza zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f75ed-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f75ed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f75ed-107">EXAMPLES</span></span>

### <span data-ttu-id="f75ed-108">Przykład 1. Wyłącz zasady usuwania zasad przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="f75ed-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="f75ed-109">To polecenie wyłącza zasady usuwania zasad przechowywania dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="f75ed-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="f75ed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f75ed-110">PARAMETERS</span></span>

### <span data-ttu-id="f75ed-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f75ed-111">-Context</span></span>
<span data-ttu-id="f75ed-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="f75ed-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f75ed-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f75ed-113">-PassThru</span></span>
<span data-ttu-id="f75ed-114">Wyświetlanie DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="f75ed-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="f75ed-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f75ed-115">-Confirm</span></span>
<span data-ttu-id="f75ed-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75ed-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75ed-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75ed-117">-WhatIf</span></span>
<span data-ttu-id="f75ed-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75ed-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f75ed-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f75ed-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75ed-120">CommonParameters</span></span>
<span data-ttu-id="f75ed-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75ed-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75ed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75ed-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f75ed-123">INPUTS</span></span>

### <span data-ttu-id="f75ed-124">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f75ed-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f75ed-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f75ed-125">OUTPUTS</span></span>

### <span data-ttu-id="f75ed-126">Microsoft. platformy windowsazure. Commands. Storage. model. resourcemode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="f75ed-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="f75ed-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f75ed-127">NOTES</span></span>

## <span data-ttu-id="f75ed-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f75ed-128">RELATED LINKS</span></span>

