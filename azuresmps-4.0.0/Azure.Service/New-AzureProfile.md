---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054966"
---
# <span data-ttu-id="be317-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="be317-101">New-AzureProfile</span></span>

## <span data-ttu-id="be317-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be317-102">SYNOPSIS</span></span>

## <span data-ttu-id="be317-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be317-103">SYNTAX</span></span>

### <span data-ttu-id="be317-104">Dyplom</span><span class="sxs-lookup"><span data-stu-id="be317-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="be317-105">Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="be317-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="be317-106">Klucza</span><span class="sxs-lookup"><span data-stu-id="be317-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="be317-107">Uprawnienia</span><span class="sxs-lookup"><span data-stu-id="be317-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="be317-108">Wolnego</span><span class="sxs-lookup"><span data-stu-id="be317-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="be317-109">Plik</span><span class="sxs-lookup"><span data-stu-id="be317-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="be317-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="be317-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="be317-111">Opis</span><span class="sxs-lookup"><span data-stu-id="be317-111">DESCRIPTION</span></span>

## <span data-ttu-id="be317-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be317-112">EXAMPLES</span></span>

### <span data-ttu-id="be317-113">1:1</span><span class="sxs-lookup"><span data-stu-id="be317-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="be317-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be317-114">PARAMETERS</span></span>

### <span data-ttu-id="be317-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="be317-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="be317-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="be317-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be317-118">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="be317-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-119">-Środowisko</span><span class="sxs-lookup"><span data-stu-id="be317-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-120">-Path</span><span class="sxs-lookup"><span data-stu-id="be317-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="be317-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-122">-Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="be317-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="be317-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="be317-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-125">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="be317-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be317-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be317-126">CommonParameters</span></span>
<span data-ttu-id="be317-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be317-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be317-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be317-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be317-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be317-129">INPUTS</span></span>

## <span data-ttu-id="be317-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be317-130">OUTPUTS</span></span>

## <span data-ttu-id="be317-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be317-131">NOTES</span></span>

## <span data-ttu-id="be317-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be317-132">RELATED LINKS</span></span>

