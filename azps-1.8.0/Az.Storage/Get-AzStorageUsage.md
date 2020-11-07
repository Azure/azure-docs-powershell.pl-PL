---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 31729843425f2360f1716e2b0faffc72715b9a81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707605"
---
# <span data-ttu-id="51122-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="51122-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="51122-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51122-102">SYNOPSIS</span></span>
<span data-ttu-id="51122-103">Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51122-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="51122-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51122-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51122-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51122-105">DESCRIPTION</span></span>
<span data-ttu-id="51122-106">Polecenie cmdlet **Get-AzStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51122-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="51122-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51122-107">EXAMPLES</span></span>

### <span data-ttu-id="51122-108">Przykład 1: uzyskiwanie użycia zasobów magazynowania w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="51122-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="51122-109">To polecenie uzyskuje użycie zasobów magazynowania w określonej lokalizacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51122-109">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="51122-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51122-110">PARAMETERS</span></span>

### <span data-ttu-id="51122-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51122-111">-DefaultProfile</span></span>
<span data-ttu-id="51122-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51122-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51122-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="51122-113">-Location</span></span>
<span data-ttu-id="51122-114">Wskaż, aby pobrać użycie zasobów magazynowania w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="51122-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="51122-115">Jeśli nie określono tego pola, będziesz mieć dostęp do zasobów magazynowania we wszystkich lokalizacjach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="51122-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51122-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51122-116">CommonParameters</span></span>
<span data-ttu-id="51122-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51122-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51122-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51122-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51122-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51122-119">INPUTS</span></span>

### <span data-ttu-id="51122-120">System. String</span><span class="sxs-lookup"><span data-stu-id="51122-120">System.String</span></span>

## <span data-ttu-id="51122-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51122-121">OUTPUTS</span></span>

### <span data-ttu-id="51122-122">Microsoft. Azure. Commands. Management. Storage. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="51122-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="51122-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51122-123">NOTES</span></span>

## <span data-ttu-id="51122-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51122-124">RELATED LINKS</span></span>

[<span data-ttu-id="51122-125">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="51122-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


