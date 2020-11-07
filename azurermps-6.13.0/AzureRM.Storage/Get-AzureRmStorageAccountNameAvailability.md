---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 402e3fdfe108486cd356af8a20ea06793f533937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551975"
---
# <span data-ttu-id="dcf5d-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="dcf5d-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="dcf5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcf5d-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf5d-103">Sprawdza dostępność nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dcf5d-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcf5d-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dcf5d-105">DESCRIPTION</span></span>
<span data-ttu-id="dcf5d-106">Polecenie cmdlet **Get-AzureRmStorageAccountNameAvailability** sprawdza, czy nazwa konta usługi Azure Storage jest prawidłowa i dostępna do użytku.</span><span class="sxs-lookup"><span data-stu-id="dcf5d-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="dcf5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcf5d-107">EXAMPLES</span></span>

### <span data-ttu-id="dcf5d-108">Przykład 1: Sprawdzanie dostępności nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="dcf5d-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="dcf5d-109">To polecenie sprawdza dostępność nazwy ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="dcf5d-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="dcf5d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcf5d-110">PARAMETERS</span></span>

### <span data-ttu-id="dcf5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf5d-111">-DefaultProfile</span></span>
<span data-ttu-id="dcf5d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf5d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf5d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcf5d-113">-Name</span></span>
<span data-ttu-id="dcf5d-114">Określa nazwę konta magazynu, które jest sprawdzane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcf5d-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="dcf5d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf5d-115">CommonParameters</span></span>
<span data-ttu-id="dcf5d-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf5d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf5d-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf5d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf5d-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcf5d-118">INPUTS</span></span>

### <span data-ttu-id="dcf5d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf5d-119">System.String</span></span>

## <span data-ttu-id="dcf5d-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcf5d-120">OUTPUTS</span></span>

### <span data-ttu-id="dcf5d-121">Microsoft. Azure. Management. Storage. MODELES. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="dcf5d-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="dcf5d-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcf5d-122">NOTES</span></span>

## <span data-ttu-id="dcf5d-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcf5d-123">RELATED LINKS</span></span>

[<span data-ttu-id="dcf5d-124">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="dcf5d-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)

