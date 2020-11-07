---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892186"
---
# <span data-ttu-id="3de38-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3de38-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="3de38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3de38-102">SYNOPSIS</span></span>
<span data-ttu-id="3de38-103">Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3de38-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="3de38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3de38-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3de38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3de38-105">DESCRIPTION</span></span>
<span data-ttu-id="3de38-106">Polecenie cmdlet **Get-AzStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3de38-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="3de38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3de38-107">EXAMPLES</span></span>

### <span data-ttu-id="3de38-108">Przykład 1: uzyskiwanie użycia zasobów magazynowania</span><span class="sxs-lookup"><span data-stu-id="3de38-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="3de38-109">To polecenie umożliwia pobieranie zasobów magazynowania dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3de38-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="3de38-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3de38-110">PARAMETERS</span></span>

### <span data-ttu-id="3de38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de38-111">-DefaultProfile</span></span>
<span data-ttu-id="3de38-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3de38-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3de38-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de38-113">CommonParameters</span></span>
<span data-ttu-id="3de38-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de38-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de38-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de38-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de38-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3de38-116">INPUTS</span></span>

### <span data-ttu-id="3de38-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3de38-117">None</span></span>

## <span data-ttu-id="3de38-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3de38-118">OUTPUTS</span></span>

### <span data-ttu-id="3de38-119">Microsoft. Azure. Commands. Management. Storage. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="3de38-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="3de38-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3de38-120">NOTES</span></span>

## <span data-ttu-id="3de38-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3de38-121">RELATED LINKS</span></span>

[<span data-ttu-id="3de38-122">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="3de38-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


