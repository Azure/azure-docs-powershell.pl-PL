---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547316"
---
# <span data-ttu-id="e1c0d-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e1c0d-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="e1c0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c0d-103">Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1c0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1c0d-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1c0d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c0d-106">Polecenie cmdlet **Get-AzureRmStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="e1c0d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1c0d-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c0d-108">Przykład 1: uzyskiwanie użycia zasobów magazynowania</span><span class="sxs-lookup"><span data-stu-id="e1c0d-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="e1c0d-109">To polecenie umożliwia pobieranie zasobów magazynowania dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="e1c0d-110">Przykład 2: uzyskiwanie użycia zasobów magazynowania w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="e1c0d-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="e1c0d-111">To polecenie uzyskuje użycie zasobów magazynowania w określonej lokalizacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="e1c0d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1c0d-112">PARAMETERS</span></span>

### <span data-ttu-id="e1c0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c0d-113">-DefaultProfile</span></span>
<span data-ttu-id="e1c0d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c0d-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e1c0d-115">-Location</span></span>
<span data-ttu-id="e1c0d-116">Wskaż, aby pobrać użycie zasobów magazynowania w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="e1c0d-117">Jeśli nie określono tego pola, będziesz mieć dostęp do zasobów magazynowania we wszystkich lokalizacjach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c0d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c0d-118">CommonParameters</span></span>
<span data-ttu-id="e1c0d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c0d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c0d-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c0d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c0d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1c0d-121">INPUTS</span></span>

### <span data-ttu-id="e1c0d-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1c0d-122">None</span></span>

## <span data-ttu-id="e1c0d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1c0d-123">OUTPUTS</span></span>

### <span data-ttu-id="e1c0d-124">Microsoft. Azure. Commands. Management. Storage. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="e1c0d-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="e1c0d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1c0d-125">NOTES</span></span>

## <span data-ttu-id="e1c0d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1c0d-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1c0d-127">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="e1c0d-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


