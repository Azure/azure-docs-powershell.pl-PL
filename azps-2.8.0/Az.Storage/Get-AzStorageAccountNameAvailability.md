---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 60e30de4d6d55007ec659a267b1d450ac1cfeff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887841"
---
# <span data-ttu-id="dd98c-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="dd98c-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="dd98c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd98c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd98c-103">Sprawdza dostępność nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dd98c-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="dd98c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd98c-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd98c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd98c-105">DESCRIPTION</span></span>
<span data-ttu-id="dd98c-106">Polecenie cmdlet **Get-AzStorageAccountNameAvailability** sprawdza, czy nazwa konta usługi Azure Storage jest prawidłowa i dostępna do użytku.</span><span class="sxs-lookup"><span data-stu-id="dd98c-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="dd98c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd98c-107">EXAMPLES</span></span>

### <span data-ttu-id="dd98c-108">Przykład 1: Sprawdzanie dostępności nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="dd98c-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="dd98c-109">To polecenie sprawdza dostępność nazwy ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="dd98c-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="dd98c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd98c-110">PARAMETERS</span></span>

### <span data-ttu-id="dd98c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd98c-111">-DefaultProfile</span></span>
<span data-ttu-id="dd98c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd98c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd98c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd98c-113">-Name</span></span>
<span data-ttu-id="dd98c-114">Określa nazwę konta magazynu, które jest sprawdzane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd98c-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="dd98c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd98c-115">CommonParameters</span></span>
<span data-ttu-id="dd98c-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd98c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd98c-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd98c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd98c-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd98c-118">INPUTS</span></span>

### <span data-ttu-id="dd98c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="dd98c-119">System.String</span></span>

## <span data-ttu-id="dd98c-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd98c-120">OUTPUTS</span></span>

### <span data-ttu-id="dd98c-121">Microsoft. Azure. Management. Storage. MODELES. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="dd98c-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="dd98c-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd98c-122">NOTES</span></span>

## <span data-ttu-id="dd98c-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd98c-123">RELATED LINKS</span></span>

[<span data-ttu-id="dd98c-124">Polecenia cmdlet usługi Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="dd98c-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


