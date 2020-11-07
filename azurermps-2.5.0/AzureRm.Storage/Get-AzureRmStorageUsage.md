---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898138"
---
# <span data-ttu-id="a3938-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a3938-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="a3938-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3938-102">SYNOPSIS</span></span>
<span data-ttu-id="a3938-103">Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3938-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3938-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3938-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3938-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3938-105">DESCRIPTION</span></span>
<span data-ttu-id="a3938-106">Polecenie cmdlet **Get-AzureRmStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3938-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="a3938-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3938-107">EXAMPLES</span></span>

### <span data-ttu-id="a3938-108">Przykład 1: uzyskiwanie użycia zasobów magazynowania</span><span class="sxs-lookup"><span data-stu-id="a3938-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="a3938-109">To polecenie umożliwia pobieranie zasobów magazynowania dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a3938-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="a3938-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3938-110">PARAMETERS</span></span>

### <span data-ttu-id="a3938-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3938-111">-DefaultProfile</span></span>
<span data-ttu-id="a3938-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3938-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3938-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3938-113">CommonParameters</span></span>
<span data-ttu-id="a3938-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3938-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3938-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3938-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3938-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3938-116">INPUTS</span></span>

### <span data-ttu-id="a3938-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3938-117">None</span></span>

## <span data-ttu-id="a3938-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3938-118">OUTPUTS</span></span>

### <span data-ttu-id="a3938-119">Microsoft. Azure. Commands. Management. Storage. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="a3938-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="a3938-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3938-120">NOTES</span></span>

## <span data-ttu-id="a3938-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3938-121">RELATED LINKS</span></span>

[<span data-ttu-id="a3938-122">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="a3938-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


