---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333169"
---
# <span data-ttu-id="e0436-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="e0436-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="e0436-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0436-102">SYNOPSIS</span></span>
<span data-ttu-id="e0436-103">Uzyskaj token dostępu surowego.</span><span class="sxs-lookup"><span data-stu-id="e0436-103">Get raw access token.</span></span> <span data-ttu-id="e0436-104">Gdy korzystasz z funkcji-ResourceUrl, upewnij się, że wartość jest zgodna z bieżącym środowiskiem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0436-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="e0436-105">Możesz odwołać się do wartości `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="e0436-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="e0436-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0436-106">SYNTAX</span></span>

### <span data-ttu-id="e0436-107">KnownResourceTypeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e0436-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0436-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="e0436-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0436-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e0436-109">DESCRIPTION</span></span>
<span data-ttu-id="e0436-110">Uzyskaj token dostępu</span><span class="sxs-lookup"><span data-stu-id="e0436-110">Get access token</span></span>

## <span data-ttu-id="e0436-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0436-111">EXAMPLES</span></span>

### <span data-ttu-id="e0436-112">Przykład 1 Uzyskaj token dostępu surowego dla punktu końcowego ARM</span><span class="sxs-lookup"><span data-stu-id="e0436-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="e0436-113">Uzyskiwanie tokenu dostępu dla punktu końcowego programu Access dla bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="e0436-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="e0436-114">Przykład 2 Uzyskaj token dostępu surowego dla punktu końcowego wykresu w usłudze AAD</span><span class="sxs-lookup"><span data-stu-id="e0436-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="e0436-115">Uzyskiwanie tokenu dostępu dla punktu końcowego programu Access Graph dla bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="e0436-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="e0436-116">Przykład 3 Uzyskaj token dostępu surowego dla punktu końcowego wykresu w usłudze AAD</span><span class="sxs-lookup"><span data-stu-id="e0436-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="e0436-117">Uzyskiwanie tokenu dostępu dla punktu końcowego programu Access Graph dla bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="e0436-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="e0436-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0436-118">PARAMETERS</span></span>

### <span data-ttu-id="e0436-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0436-119">-DefaultProfile</span></span>
<span data-ttu-id="e0436-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0436-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0436-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="e0436-121">-ResourceTypeName</span></span>
<span data-ttu-id="e0436-122">Opcjonalna nazwa typu Resouce, obsługiwane wartości: AadGraph, AnalysisServices, ARM, atestacja, partia, datalake, magazyn, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="e0436-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="e0436-123">Wartość domyślna to ramię, jeśli nie zostało określone.</span><span class="sxs-lookup"><span data-stu-id="e0436-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0436-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="e0436-124">-ResourceUrl</span></span>
<span data-ttu-id="e0436-125">Adres URL zasobu, dla którego żądasz tokenu, na przykład ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="e0436-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0436-126">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e0436-126">-TenantId</span></span>
<span data-ttu-id="e0436-127">Opcjonalny identyfikator dzierżawy. Użyj identyfikatora dzierżawy domyślnego, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="e0436-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0436-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0436-128">CommonParameters</span></span>
<span data-ttu-id="e0436-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0436-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0436-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0436-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0436-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0436-131">INPUTS</span></span>

### <span data-ttu-id="e0436-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e0436-132">None</span></span>

## <span data-ttu-id="e0436-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0436-133">OUTPUTS</span></span>

### <span data-ttu-id="e0436-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e0436-134">System.String</span></span>

## <span data-ttu-id="e0436-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0436-135">NOTES</span></span>

## <span data-ttu-id="e0436-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0436-136">RELATED LINKS</span></span>
