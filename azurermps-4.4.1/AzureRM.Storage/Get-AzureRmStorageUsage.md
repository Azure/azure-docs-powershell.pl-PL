---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: 1ef273329634e080c4117b9ddd0d1eaf8d91bb0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719493"
---
# <span data-ttu-id="3007c-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3007c-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="3007c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3007c-102">SYNOPSIS</span></span>
<span data-ttu-id="3007c-103">Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3007c-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3007c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3007c-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3007c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3007c-105">DESCRIPTION</span></span>
<span data-ttu-id="3007c-106">Polecenie cmdlet **Get-AzureRmStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3007c-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="3007c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3007c-107">EXAMPLES</span></span>

### <span data-ttu-id="3007c-108">Przykład 1: uzyskiwanie użycia zasobów magazynowania</span><span class="sxs-lookup"><span data-stu-id="3007c-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="3007c-109">To polecenie umożliwia pobieranie zasobów magazynowania dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3007c-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="3007c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3007c-110">PARAMETERS</span></span>

### <span data-ttu-id="3007c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3007c-111">-DefaultProfile</span></span>
<span data-ttu-id="3007c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3007c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3007c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3007c-113">CommonParameters</span></span>
<span data-ttu-id="3007c-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3007c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3007c-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3007c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3007c-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3007c-116">INPUTS</span></span>

## <span data-ttu-id="3007c-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3007c-117">OUTPUTS</span></span>

## <span data-ttu-id="3007c-118">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3007c-118">NOTES</span></span>

## <span data-ttu-id="3007c-119">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3007c-119">RELATED LINKS</span></span>

[<span data-ttu-id="3007c-120">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="3007c-120">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


