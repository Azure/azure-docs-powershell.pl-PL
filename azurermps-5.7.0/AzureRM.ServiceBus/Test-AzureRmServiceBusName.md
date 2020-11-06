---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542271"
---
# <span data-ttu-id="0c0db-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="0c0db-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="0c0db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c0db-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0db-103">Sprawdza dostępność danej nazwy obszaru nazw lub aliasu (nazwy konfiguracji DR).</span><span class="sxs-lookup"><span data-stu-id="0c0db-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c0db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c0db-104">SYNTAX</span></span>

### <span data-ttu-id="0c0db-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0c0db-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c0db-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0c0db-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c0db-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c0db-107">DESCRIPTION</span></span>
<span data-ttu-id="0c0db-108">Polecenie cmdlet **test-AzureRmServiceBusName** sprawdza dostępność nazwy obszaru nazw lub aliasu (nazwy konfiguracji dr).</span><span class="sxs-lookup"><span data-stu-id="0c0db-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="0c0db-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c0db-109">EXAMPLES</span></span>

### <span data-ttu-id="0c0db-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c0db-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0c0db-111">Zwraca stan dostępności nazwy obszaru nazw "MyNameSapceName" jako prawda.</span><span class="sxs-lookup"><span data-stu-id="0c0db-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="0c0db-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0c0db-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="0c0db-113">Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako FAŁSZ z powodu</span><span class="sxs-lookup"><span data-stu-id="0c0db-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="0c0db-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0c0db-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="0c0db-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c0db-115">PARAMETERS</span></span>

### <span data-ttu-id="0c0db-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="0c0db-116">-AliasName</span></span>
<span data-ttu-id="0c0db-117">Nazwa konfiguracji DR — Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="0c0db-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c0db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0db-118">-DefaultProfile</span></span>
<span data-ttu-id="0c0db-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c0db-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c0db-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c0db-120">-Namespace</span></span>
<span data-ttu-id="0c0db-121">Nazwa przestrzeni nazw ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0c0db-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c0db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c0db-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c0db-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0c0db-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c0db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0db-124">CommonParameters</span></span>
<span data-ttu-id="0c0db-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c0db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0c0db-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0db-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c0db-127">INPUTS</span></span>

### <span data-ttu-id="0c0db-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0c0db-128">System.String</span></span>


## <span data-ttu-id="0c0db-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c0db-129">OUTPUTS</span></span>

### <span data-ttu-id="0c0db-130">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0c0db-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="0c0db-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c0db-131">NOTES</span></span>

## <span data-ttu-id="0c0db-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c0db-132">RELATED LINKS</span></span>
