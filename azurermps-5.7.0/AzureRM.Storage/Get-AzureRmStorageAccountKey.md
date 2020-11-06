---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526521"
---
# <span data-ttu-id="e1a06-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e1a06-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="e1a06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1a06-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a06-103">Pobiera klucze dostępu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1a06-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1a06-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="e1a06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1a06-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a06-106">Polecenie cmdlet **Get-AzureRmStorageAccountKey** pobiera klucze dostępu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1a06-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="e1a06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1a06-107">EXAMPLES</span></span>

### <span data-ttu-id="e1a06-108">Przykład 1: uzyskiwanie klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e1a06-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="e1a06-109">To polecenie pobiera klucze określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1a06-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="e1a06-110">Przykład 2: uzyskiwanie określonego klucza dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e1a06-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="e1a06-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1a06-111">PARAMETERS</span></span>

### <span data-ttu-id="e1a06-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1a06-112">-Name</span></span>
<span data-ttu-id="e1a06-113">Określa nazwę konta magazynu, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="e1a06-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="e1a06-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a06-114">-ResourceGroupName</span></span>
<span data-ttu-id="e1a06-115">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="e1a06-115">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a06-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a06-116">CommonParameters</span></span>
<span data-ttu-id="e1a06-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a06-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a06-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a06-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a06-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1a06-119">INPUTS</span></span>

### <span data-ttu-id="e1a06-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1a06-120">None</span></span>
<span data-ttu-id="e1a06-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e1a06-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1a06-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1a06-122">OUTPUTS</span></span>

## <span data-ttu-id="e1a06-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1a06-123">NOTES</span></span>

## <span data-ttu-id="e1a06-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1a06-124">RELATED LINKS</span></span>

[<span data-ttu-id="e1a06-125">Nowe — AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e1a06-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
