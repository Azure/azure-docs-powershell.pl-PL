---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 7cd67b98b91a03e47ecefba7f329655895972913
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892258"
---
# <span data-ttu-id="b6ba6-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6ba6-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="b6ba6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ba6-103">Pobieranie właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b6ba6-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="b6ba6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6ba6-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6ba6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6ba6-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ba6-106">Polecenie cmdlet **Get-AzStorageAccountNetworkRuleSet** Pobiera właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b6ba6-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b6ba6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6ba6-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ba6-108">Przykład 1: pobieranie właściwości NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b6ba6-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="b6ba6-109">To polecenie pobiera właściwość NetworkRule określonego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b6ba6-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="b6ba6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6ba6-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ba6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ba6-111">-DefaultProfile</span></span>
<span data-ttu-id="b6ba6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ba6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6ba6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6ba6-113">-Name</span></span>
<span data-ttu-id="b6ba6-114">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6ba6-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="b6ba6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ba6-115">-ResourceGroupName</span></span>
<span data-ttu-id="b6ba6-116">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6ba6-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="b6ba6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ba6-117">CommonParameters</span></span>
<span data-ttu-id="b6ba6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ba6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ba6-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ba6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ba6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6ba6-120">INPUTS</span></span>

### <span data-ttu-id="b6ba6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b6ba6-121">System.String</span></span>

## <span data-ttu-id="b6ba6-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6ba6-122">OUTPUTS</span></span>

### <span data-ttu-id="b6ba6-123">Microsoft. Azure. Commands. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6ba6-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="b6ba6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6ba6-124">NOTES</span></span>

## <span data-ttu-id="b6ba6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6ba6-125">RELATED LINKS</span></span>
