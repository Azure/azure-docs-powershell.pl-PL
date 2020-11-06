---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546011"
---
# <span data-ttu-id="291be-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="291be-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="291be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="291be-102">SYNOPSIS</span></span>
<span data-ttu-id="291be-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="291be-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="291be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="291be-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="291be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="291be-105">DESCRIPTION</span></span>
<span data-ttu-id="291be-106">Polecenie cmdlet **Get-AzureRmServiceBusNamespaceKey** zwraca podstawowe i pomocnicze ciągi połączeń dla danego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="291be-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="291be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="291be-107">EXAMPLES</span></span>

### <span data-ttu-id="291be-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="291be-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="291be-109">Podstawowy i pomocniczy ciąg połączenia z określoną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="291be-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="291be-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="291be-110">PARAMETERS</span></span>

### <span data-ttu-id="291be-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="291be-111">-ResourceGroup</span></span>
<span data-ttu-id="291be-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="291be-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="291be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291be-113">-DefaultProfile</span></span>
<span data-ttu-id="291be-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="291be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="291be-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="291be-115">-Name</span></span>
<span data-ttu-id="291be-116">ServiceBus przestrzeń nazw AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="291be-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="291be-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="291be-117">-Namespace</span></span>
<span data-ttu-id="291be-118">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="291be-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="291be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291be-119">CommonParameters</span></span>
<span data-ttu-id="291be-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="291be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291be-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291be-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291be-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="291be-122">INPUTS</span></span>

### <span data-ttu-id="291be-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="291be-123">-ResourceGroup</span></span>
 <span data-ttu-id="291be-124">System. String</span><span class="sxs-lookup"><span data-stu-id="291be-124">System.String</span></span>
 

### <span data-ttu-id="291be-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="291be-125">-NamespaceName</span></span>
 <span data-ttu-id="291be-126">System. String</span><span class="sxs-lookup"><span data-stu-id="291be-126">System.String</span></span>
 

### <span data-ttu-id="291be-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="291be-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="291be-128">System. String</span><span class="sxs-lookup"><span data-stu-id="291be-128">System.String</span></span>

## <span data-ttu-id="291be-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="291be-129">OUTPUTS</span></span>

### <span data-ttu-id="291be-130">Microsoft. Azure. Management. ServiceBus. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="291be-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="291be-131">PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey wartość} SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey wartość} PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey wartość} NazwaKlucza: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="291be-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="291be-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="291be-132">NOTES</span></span>

## <span data-ttu-id="291be-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="291be-133">RELATED LINKS</span></span>

