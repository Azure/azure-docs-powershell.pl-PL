---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 6620579ad49143dc715fc62f23d305e2efd3d5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007889"
---
# <span data-ttu-id="d5ce4-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="d5ce4-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="d5ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ce4-103">Sprawdza dostępność danej nazwy lub aliasu NameSpace (nazwa konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="d5ce4-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="d5ce4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5ce4-104">SYNTAX</span></span>

### <span data-ttu-id="d5ce4-105">NamespaceCheckNameAvailabilitySet (Default)</span><span class="sxs-lookup"><span data-stu-id="d5ce4-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5ce4-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d5ce4-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5ce4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="d5ce4-108">Polecenie **cmdlet Test-azEventhubName** sprawdza dostępność nazwy lub aliasu NameSpace (nazwa konfiguracji DR)</span><span class="sxs-lookup"><span data-stu-id="d5ce4-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="d5ce4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5ce4-109">EXAMPLES</span></span>

### <span data-ttu-id="d5ce4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5ce4-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d5ce4-111">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako Prawda, jeśli jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="d5ce4-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="d5ce4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d5ce4-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d5ce4-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako Fałsz z powodu.</span><span class="sxs-lookup"><span data-stu-id="d5ce4-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="d5ce4-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d5ce4-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="d5ce4-115">Zwraca stan dostępności nazwy aliasu "myAliasName" dla przestrzeni nazw "MyNameSapceName" jako prawda, jeśli jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="d5ce4-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="d5ce4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5ce4-116">PARAMETERS</span></span>

### <span data-ttu-id="d5ce4-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="d5ce4-117">-AliasName</span></span>
<span data-ttu-id="d5ce4-118">Nazwa konfiguracji dr — nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="d5ce4-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="d5ce4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ce4-119">-DefaultProfile</span></span>
<span data-ttu-id="d5ce4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ce4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ce4-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="d5ce4-121">-Namespace</span></span>
<span data-ttu-id="d5ce4-122">Nazwa przestrzeni nazw aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="d5ce4-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="d5ce4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ce4-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5ce4-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d5ce4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d5ce4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ce4-125">CommonParameters</span></span>
<span data-ttu-id="d5ce4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ce4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ce4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ce4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ce4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5ce4-128">INPUTS</span></span>

### <span data-ttu-id="d5ce4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d5ce4-129">System.String</span></span>

## <span data-ttu-id="d5ce4-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5ce4-130">OUTPUTS</span></span>

### <span data-ttu-id="d5ce4-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="d5ce4-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="d5ce4-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5ce4-132">NOTES</span></span>

## <span data-ttu-id="d5ce4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5ce4-133">RELATED LINKS</span></span>
