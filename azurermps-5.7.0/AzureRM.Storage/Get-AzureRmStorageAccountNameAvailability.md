---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716607"
---
# <span data-ttu-id="630c2-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="630c2-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="630c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="630c2-102">SYNOPSIS</span></span>
<span data-ttu-id="630c2-103">Sprawdza dostępność nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="630c2-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="630c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="630c2-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="630c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="630c2-105">DESCRIPTION</span></span>
<span data-ttu-id="630c2-106">Polecenie cmdlet **Get-AzureRmStorageAccountNameAvailability** sprawdza, czy nazwa konta usługi Azure Storage jest prawidłowa i dostępna do użytku.</span><span class="sxs-lookup"><span data-stu-id="630c2-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="630c2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="630c2-107">EXAMPLES</span></span>

### <span data-ttu-id="630c2-108">Przykład 1: Sprawdzanie dostępności nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="630c2-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="630c2-109">To polecenie sprawdza dostępność nazwy ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="630c2-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="630c2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="630c2-110">PARAMETERS</span></span>

### <span data-ttu-id="630c2-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="630c2-111">-Name</span></span>
<span data-ttu-id="630c2-112">Określa nazwę konta magazynu, które jest sprawdzane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="630c2-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="630c2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630c2-113">CommonParameters</span></span>
<span data-ttu-id="630c2-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630c2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630c2-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630c2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630c2-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="630c2-116">INPUTS</span></span>

### <span data-ttu-id="630c2-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="630c2-117">None</span></span>
<span data-ttu-id="630c2-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="630c2-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="630c2-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="630c2-119">OUTPUTS</span></span>

## <span data-ttu-id="630c2-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="630c2-120">NOTES</span></span>

## <span data-ttu-id="630c2-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="630c2-121">RELATED LINKS</span></span>

[<span data-ttu-id="630c2-122">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="630c2-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)
