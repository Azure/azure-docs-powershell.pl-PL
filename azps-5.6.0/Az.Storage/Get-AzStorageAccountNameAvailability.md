---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 6e4582a8963f3d57bacd3dfb9c869368986c5668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002778"
---
# <span data-ttu-id="87022-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="87022-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="87022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87022-102">SYNOPSIS</span></span>
<span data-ttu-id="87022-103">Sprawdza dostępność nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="87022-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="87022-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87022-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87022-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87022-105">DESCRIPTION</span></span>
<span data-ttu-id="87022-106">Polecenie **cmdlet Get-AzStorageAccountNameAvailability** sprawdza, czy nazwa konta usługi Azure Storage jest prawidłowa i dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="87022-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="87022-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87022-107">EXAMPLES</span></span>

### <span data-ttu-id="87022-108">Przykład 1. Sprawdzanie dostępności nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="87022-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="87022-109">To polecenie sprawdza dostępność nazwy ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="87022-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="87022-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87022-110">PARAMETERS</span></span>

### <span data-ttu-id="87022-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87022-111">-DefaultProfile</span></span>
<span data-ttu-id="87022-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87022-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87022-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87022-113">-Name</span></span>
<span data-ttu-id="87022-114">Określa nazwę konta magazynu sprawdzane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87022-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87022-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87022-115">CommonParameters</span></span>
<span data-ttu-id="87022-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87022-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87022-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87022-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87022-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87022-118">INPUTS</span></span>

### <span data-ttu-id="87022-119">System.String</span><span class="sxs-lookup"><span data-stu-id="87022-119">System.String</span></span>

## <span data-ttu-id="87022-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87022-120">OUTPUTS</span></span>

### <span data-ttu-id="87022-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="87022-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="87022-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87022-122">NOTES</span></span>

## <span data-ttu-id="87022-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87022-123">RELATED LINKS</span></span>

[<span data-ttu-id="87022-124">Polecenia cmdlet menedżera magazynowania platformy Azure</span><span class="sxs-lookup"><span data-stu-id="87022-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


