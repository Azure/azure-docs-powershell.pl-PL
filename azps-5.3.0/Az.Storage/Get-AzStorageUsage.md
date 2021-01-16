---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376229"
---
# <span data-ttu-id="6da95-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6da95-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="6da95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6da95-102">SYNOPSIS</span></span>
<span data-ttu-id="6da95-103">Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6da95-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="6da95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6da95-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6da95-105">DESCRIPTION</span></span>
<span data-ttu-id="6da95-106">Polecenie cmdlet **Get-AzStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6da95-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="6da95-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6da95-107">EXAMPLES</span></span>

### <span data-ttu-id="6da95-108">Przykład 1: uzyskiwanie użycia zasobów magazynowania w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="6da95-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="6da95-109">To polecenie uzyskuje użycie zasobów magazynu w określonej lokalizacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6da95-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="6da95-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6da95-110">PARAMETERS</span></span>

### <span data-ttu-id="6da95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da95-111">-DefaultProfile</span></span>
<span data-ttu-id="6da95-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6da95-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6da95-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6da95-113">-Location</span></span>
<span data-ttu-id="6da95-114">Wskaż, aby pobrać użycie zasobów magazynowania w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="6da95-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="6da95-115">Jeśli nie określono tego pola, będziesz mieć dostęp do zasobów magazynowania we wszystkich lokalizacjach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="6da95-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="6da95-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da95-116">CommonParameters</span></span>
<span data-ttu-id="6da95-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da95-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da95-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da95-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da95-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6da95-119">INPUTS</span></span>

### <span data-ttu-id="6da95-120">System. String</span><span class="sxs-lookup"><span data-stu-id="6da95-120">System.String</span></span>

## <span data-ttu-id="6da95-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6da95-121">OUTPUTS</span></span>

### <span data-ttu-id="6da95-122">Microsoft. Azure. Commands. Management. Storage. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="6da95-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="6da95-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6da95-123">NOTES</span></span>

## <span data-ttu-id="6da95-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6da95-124">RELATED LINKS</span></span>

[<span data-ttu-id="6da95-125">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="6da95-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


