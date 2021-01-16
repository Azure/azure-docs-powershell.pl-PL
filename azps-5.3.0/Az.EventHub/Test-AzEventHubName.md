---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501058"
---
# <span data-ttu-id="aff11-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="aff11-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="aff11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aff11-102">SYNOPSIS</span></span>
<span data-ttu-id="aff11-103">Sprawdza dostępność danej nazwy obszaru nazw lub aliasu (nazwy konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="aff11-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="aff11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aff11-104">SYNTAX</span></span>

### <span data-ttu-id="aff11-105">NamespaceCheckNameAvailabilitySet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aff11-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aff11-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aff11-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aff11-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aff11-107">DESCRIPTION</span></span>
<span data-ttu-id="aff11-108">Polecenie cmdlet **test-AzEventhubName** sprawdza dostępność nazwy obszaru nazw lub aliasu (nazwy konfiguracji dr).</span><span class="sxs-lookup"><span data-stu-id="aff11-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="aff11-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aff11-109">EXAMPLES</span></span>

### <span data-ttu-id="aff11-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aff11-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="aff11-111">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako prawda, jeśli jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="aff11-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="aff11-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="aff11-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="aff11-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako FAŁSZ z powodu</span><span class="sxs-lookup"><span data-stu-id="aff11-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="aff11-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="aff11-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="aff11-115">Zwraca stan dostępności nazwy aliasu "aliasname" dla obszaru nazw "MyNameSapceName" jako prawda, jeśli jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="aff11-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="aff11-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aff11-116">PARAMETERS</span></span>

### <span data-ttu-id="aff11-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="aff11-117">-AliasName</span></span>
<span data-ttu-id="aff11-118">Nazwa konfiguracji DR — Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="aff11-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff11-119">-DefaultProfile</span></span>
<span data-ttu-id="aff11-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aff11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff11-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aff11-121">-Namespace</span></span>
<span data-ttu-id="aff11-122">Nazwa obszaru nazw Eventhub</span><span class="sxs-lookup"><span data-stu-id="aff11-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="aff11-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff11-123">-ResourceGroupName</span></span>
<span data-ttu-id="aff11-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aff11-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff11-125">CommonParameters</span></span>
<span data-ttu-id="aff11-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff11-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff11-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff11-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aff11-128">INPUTS</span></span>

### <span data-ttu-id="aff11-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aff11-129">System.String</span></span>

## <span data-ttu-id="aff11-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aff11-130">OUTPUTS</span></span>

### <span data-ttu-id="aff11-131">Microsoft. Azure. Commands. EventHub. modele. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="aff11-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="aff11-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aff11-132">NOTES</span></span>

## <span data-ttu-id="aff11-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aff11-133">RELATED LINKS</span></span>
