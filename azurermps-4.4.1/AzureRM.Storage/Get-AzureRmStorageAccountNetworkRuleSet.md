---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719499"
---
# <span data-ttu-id="81275-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="81275-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="81275-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81275-102">SYNOPSIS</span></span>
<span data-ttu-id="81275-103">Pobieranie właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="81275-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81275-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81275-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81275-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81275-105">DESCRIPTION</span></span>
<span data-ttu-id="81275-106">Polecenie cmdlet **Get-AzureRmStorageAccountNetworkRuleSet** Pobiera właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="81275-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="81275-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81275-107">EXAMPLES</span></span>

### <span data-ttu-id="81275-108">Przykład 1: pobieranie właściwości NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="81275-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="81275-109">To polecenie pobiera właściwość NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="81275-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="81275-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81275-110">PARAMETERS</span></span>

### <span data-ttu-id="81275-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81275-111">-Name</span></span>
<span data-ttu-id="81275-112">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="81275-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="81275-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81275-113">-ResourceGroupName</span></span>
<span data-ttu-id="81275-114">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="81275-114">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81275-115">-DefaultProfile</span></span>
<span data-ttu-id="81275-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81275-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81275-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81275-117">CommonParameters</span></span>
<span data-ttu-id="81275-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81275-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81275-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81275-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81275-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81275-120">INPUTS</span></span>

### <span data-ttu-id="81275-121">System. String</span><span class="sxs-lookup"><span data-stu-id="81275-121">System.String</span></span>

## <span data-ttu-id="81275-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81275-122">OUTPUTS</span></span>

### <span data-ttu-id="81275-123">Microsoft. Azure. Commands. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="81275-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="81275-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81275-124">NOTES</span></span>

## <span data-ttu-id="81275-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81275-125">RELATED LINKS</span></span>

