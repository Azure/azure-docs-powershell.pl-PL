---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8717019982175b30e0db84e7433147008e40803e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705408"
---
# <span data-ttu-id="08e69-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="08e69-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="08e69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08e69-102">SYNOPSIS</span></span>
<span data-ttu-id="08e69-103">Sprawdza dostępność danej nazwy obszaru nazw lub aliasu (nazwy konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="08e69-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="08e69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08e69-104">SYNTAX</span></span>

### <span data-ttu-id="08e69-105">NamespaceCheckNameAvailabilitySet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08e69-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e69-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="08e69-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e69-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08e69-107">DESCRIPTION</span></span>
<span data-ttu-id="08e69-108">Polecenie cmdlet **test-AzEventhubName** sprawdza dostępność nazwy obszaru nazw lub aliasu (nazwy konfiguracji dr).</span><span class="sxs-lookup"><span data-stu-id="08e69-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="08e69-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08e69-109">EXAMPLES</span></span>

### <span data-ttu-id="08e69-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08e69-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="08e69-111">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako prawda, jeśli jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="08e69-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="08e69-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="08e69-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="08e69-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako FAŁSZ z powodu</span><span class="sxs-lookup"><span data-stu-id="08e69-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="08e69-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="08e69-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="08e69-115">Zwraca stan dostępności nazwy aliasu "aliasname" dla obszaru nazw "MyNameSapceName" jako prawda, jeśli jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="08e69-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="08e69-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08e69-116">PARAMETERS</span></span>

### <span data-ttu-id="08e69-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="08e69-117">-AliasName</span></span>
<span data-ttu-id="08e69-118">Nazwa konfiguracji DR — Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="08e69-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="08e69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e69-119">-DefaultProfile</span></span>
<span data-ttu-id="08e69-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08e69-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e69-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="08e69-121">-Namespace</span></span>
<span data-ttu-id="08e69-122">Nazwa obszaru nazw Eventhub</span><span class="sxs-lookup"><span data-stu-id="08e69-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="08e69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e69-123">-ResourceGroupName</span></span>
<span data-ttu-id="08e69-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="08e69-124">Resource Group Name</span></span>

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

### <span data-ttu-id="08e69-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e69-125">CommonParameters</span></span>
<span data-ttu-id="08e69-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e69-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e69-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e69-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e69-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08e69-128">INPUTS</span></span>

### <span data-ttu-id="08e69-129">System. String</span><span class="sxs-lookup"><span data-stu-id="08e69-129">System.String</span></span>

## <span data-ttu-id="08e69-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08e69-130">OUTPUTS</span></span>

### <span data-ttu-id="08e69-131">Microsoft. Azure. Commands. EventHub. modele. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="08e69-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="08e69-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08e69-132">NOTES</span></span>

## <span data-ttu-id="08e69-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08e69-133">RELATED LINKS</span></span>
