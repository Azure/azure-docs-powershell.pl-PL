---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8ca5c33944882fde7e9bad2411df5f41dbe5f788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544640"
---
# <span data-ttu-id="aea38-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="aea38-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="aea38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aea38-102">SYNOPSIS</span></span>
<span data-ttu-id="aea38-103">Sprawdza dostępność nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="aea38-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aea38-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aea38-105">DESCRIPTION</span></span>
<span data-ttu-id="aea38-106">Polecenie cmdlet **Get-AzureRmStorageAccountNameAvailability** sprawdza, czy nazwa konta usługi Azure Storage jest prawidłowa i dostępna do użytku.</span><span class="sxs-lookup"><span data-stu-id="aea38-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="aea38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aea38-107">EXAMPLES</span></span>

### <span data-ttu-id="aea38-108">Przykład 1: Sprawdzanie dostępności nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="aea38-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="aea38-109">To polecenie sprawdza dostępność nazwy ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="aea38-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="aea38-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aea38-110">PARAMETERS</span></span>

### <span data-ttu-id="aea38-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aea38-111">-Name</span></span>
<span data-ttu-id="aea38-112">Określa nazwę konta magazynu, które jest sprawdzane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea38-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="aea38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea38-113">-DefaultProfile</span></span>
<span data-ttu-id="aea38-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aea38-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea38-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea38-115">CommonParameters</span></span>
<span data-ttu-id="aea38-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea38-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea38-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea38-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea38-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aea38-118">INPUTS</span></span>

## <span data-ttu-id="aea38-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aea38-119">OUTPUTS</span></span>

## <span data-ttu-id="aea38-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aea38-120">NOTES</span></span>

## <span data-ttu-id="aea38-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aea38-121">RELATED LINKS</span></span>

[<span data-ttu-id="aea38-122">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="aea38-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


