---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544328"
---
# <span data-ttu-id="c1d2a-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="c1d2a-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="c1d2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d2a-103">Sprawdza dostępność danej nazwy obszaru nazw lub aliasu (nazwy konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="c1d2a-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1d2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1d2a-104">SYNTAX</span></span>

### <span data-ttu-id="c1d2a-105">NamespaceCheckNameAvailabilitySet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c1d2a-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1d2a-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c1d2a-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1d2a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c1d2a-107">DESCRIPTION</span></span>
<span data-ttu-id="c1d2a-108">Polecenie cmdlet **test-AzureRmEventhubName** sprawdza dostępność nazwy obszaru nazw lub aliasu (nazwy konfiguracji dr).</span><span class="sxs-lookup"><span data-stu-id="c1d2a-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="c1d2a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1d2a-109">EXAMPLES</span></span>

### <span data-ttu-id="c1d2a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1d2a-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="c1d2a-111">Zwraca stan dostępności nazwy obszaru nazw "MyNameSapceName" jako prawda.</span><span class="sxs-lookup"><span data-stu-id="c1d2a-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="c1d2a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c1d2a-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="c1d2a-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako FAŁSZ z powodu</span><span class="sxs-lookup"><span data-stu-id="c1d2a-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="c1d2a-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c1d2a-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="c1d2a-115">Zwraca stan dostępności nazwy aliasu "aliasname" w obszarze nazw "MyNameSapceName" jako prawda</span><span class="sxs-lookup"><span data-stu-id="c1d2a-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="c1d2a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1d2a-116">PARAMETERS</span></span>

### <span data-ttu-id="c1d2a-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="c1d2a-117">-AliasName</span></span>
<span data-ttu-id="c1d2a-118">Nazwa konfiguracji DR — Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="c1d2a-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d2a-119">-DefaultProfile</span></span>
<span data-ttu-id="c1d2a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d2a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1d2a-121">-Namespace</span></span>
<span data-ttu-id="c1d2a-122">Nazwa obszaru nazw Eventhub</span><span class="sxs-lookup"><span data-stu-id="c1d2a-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="c1d2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1d2a-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c1d2a-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1d2a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d2a-125">CommonParameters</span></span>
<span data-ttu-id="c1d2a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d2a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c1d2a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d2a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d2a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1d2a-128">INPUTS</span></span>

### <span data-ttu-id="c1d2a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c1d2a-129">System.String</span></span>


## <span data-ttu-id="c1d2a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1d2a-130">OUTPUTS</span></span>

### <span data-ttu-id="c1d2a-131">Microsoft. Azure. Commands. EventHub. modele. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="c1d2a-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="c1d2a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1d2a-132">NOTES</span></span>

## <span data-ttu-id="c1d2a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1d2a-133">RELATED LINKS</span></span>
