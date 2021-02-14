---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237840"
---
# <span data-ttu-id="a4471-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="a4471-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="a4471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4471-102">SYNOPSIS</span></span>
<span data-ttu-id="a4471-103">Sprawdza dostępność danej nazwy lub aliasu NameSpace (nazwa konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="a4471-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a4471-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4471-104">SYNTAX</span></span>

### <span data-ttu-id="a4471-105">NamespaceCheckNameAvailabilitySet (Default)</span><span class="sxs-lookup"><span data-stu-id="a4471-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4471-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4471-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4471-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4471-107">DESCRIPTION</span></span>
<span data-ttu-id="a4471-108">Polecenie **cmdlet Test-AzEventhubName** sprawdza dostępność nazwy lub aliasu NameSpace (nazwa konfiguracji DR)</span><span class="sxs-lookup"><span data-stu-id="a4471-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a4471-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4471-109">EXAMPLES</span></span>

### <span data-ttu-id="a4471-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4471-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="a4471-111">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako Prawda, jeśli jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="a4471-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="a4471-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4471-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="a4471-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako Fałsz z powodu.</span><span class="sxs-lookup"><span data-stu-id="a4471-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="a4471-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a4471-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="a4471-115">Zwraca stan dostępności nazwy aliasu "myAliasName" dla przestrzeni nazw "MyNameSapceName" jako prawda, jeśli jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="a4471-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="a4471-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4471-116">PARAMETERS</span></span>

### <span data-ttu-id="a4471-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a4471-117">-AliasName</span></span>
<span data-ttu-id="a4471-118">Nazwa konfiguracji dr — nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="a4471-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="a4471-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4471-119">-DefaultProfile</span></span>
<span data-ttu-id="a4471-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4471-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4471-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="a4471-121">-Namespace</span></span>
<span data-ttu-id="a4471-122">Nazwa przestrzeni nazw aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="a4471-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="a4471-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4471-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4471-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a4471-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a4471-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4471-125">CommonParameters</span></span>
<span data-ttu-id="a4471-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4471-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4471-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4471-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4471-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4471-128">INPUTS</span></span>

### <span data-ttu-id="a4471-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a4471-129">System.String</span></span>

## <span data-ttu-id="a4471-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4471-130">OUTPUTS</span></span>

### <span data-ttu-id="a4471-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="a4471-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="a4471-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4471-132">NOTES</span></span>

## <span data-ttu-id="a4471-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4471-133">RELATED LINKS</span></span>
