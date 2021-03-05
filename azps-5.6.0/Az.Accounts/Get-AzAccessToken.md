---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973025"
---
# <span data-ttu-id="f77cc-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="f77cc-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="f77cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f77cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f77cc-103">Pobierz nieprzetworzone token dostępu.</span><span class="sxs-lookup"><span data-stu-id="f77cc-103">Get raw access token.</span></span> <span data-ttu-id="f77cc-104">Podczas korzystania z funkcji -ResourceUrl upewnij się, że wartość jest dopasowana do bieżącego środowiska platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f77cc-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="f77cc-105">Możesz odwołać się do wartości `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="f77cc-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="f77cc-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f77cc-106">SYNTAX</span></span>

### <span data-ttu-id="f77cc-107">KnownResourceTypeName (Default)</span><span class="sxs-lookup"><span data-stu-id="f77cc-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f77cc-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="f77cc-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f77cc-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f77cc-109">DESCRIPTION</span></span>
<span data-ttu-id="f77cc-110">Uzyskiwanie tokenu dostępu</span><span class="sxs-lookup"><span data-stu-id="f77cc-110">Get access token</span></span>

## <span data-ttu-id="f77cc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f77cc-111">EXAMPLES</span></span>

### <span data-ttu-id="f77cc-112">Przykład 1. Uzyskiwanie tokenu dostępu nieprzetworzonego dla ARM końcowego</span><span class="sxs-lookup"><span data-stu-id="f77cc-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="f77cc-113">Uzyskiwanie tokenu dostępu dla punktu końcowego usługi ResourceManager dla bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="f77cc-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="f77cc-114">Przykład 2. Uzyskiwanie tokenu dostępu nieprzetworzonego dla punktu końcowego wykresu AAD</span><span class="sxs-lookup"><span data-stu-id="f77cc-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="f77cc-115">Uzyskiwanie tokenu dostępu dla punktu końcowego wykresu AAD dla bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="f77cc-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="f77cc-116">Przykład 3. Uzyskiwanie tokenu dostępu nieprzetworzonego dla punktu końcowego wykresu AAD</span><span class="sxs-lookup"><span data-stu-id="f77cc-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="f77cc-117">Uzyskiwanie tokenu dostępu dla punktu końcowego wykresu AAD dla bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="f77cc-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="f77cc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f77cc-118">PARAMETERS</span></span>

### <span data-ttu-id="f77cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77cc-119">-DefaultProfile</span></span>
<span data-ttu-id="f77cc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f77cc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f77cc-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="f77cc-121">-ResourceTypeName</span></span>
<span data-ttu-id="f77cc-122">Opcjonalna nazwa typu ponownego użycia, obsługiwane wartości: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="f77cc-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="f77cc-123">Wartość domyślna to Arm, jeśli nie jest określona.</span><span class="sxs-lookup"><span data-stu-id="f77cc-123">Default value is Arm if not specified.</span></span>

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

### <span data-ttu-id="f77cc-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="f77cc-124">-ResourceUrl</span></span>
<span data-ttu-id="f77cc-125">Adres URL zasobu, do których żądasz tokenu, np. ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="f77cc-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

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

### <span data-ttu-id="f77cc-126">- TenantId</span><span class="sxs-lookup"><span data-stu-id="f77cc-126">-TenantId</span></span>
<span data-ttu-id="f77cc-127">Opcjonalny identyfikator dzierżawy. Użyj identyfikatora dzierżawy, jeśli nie określono kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="f77cc-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="f77cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77cc-128">CommonParameters</span></span>
<span data-ttu-id="f77cc-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77cc-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f77cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77cc-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f77cc-131">INPUTS</span></span>

### <span data-ttu-id="f77cc-132">Brak</span><span class="sxs-lookup"><span data-stu-id="f77cc-132">None</span></span>

## <span data-ttu-id="f77cc-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f77cc-133">OUTPUTS</span></span>

### <span data-ttu-id="f77cc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f77cc-134">System.String</span></span>

## <span data-ttu-id="f77cc-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f77cc-135">NOTES</span></span>

## <span data-ttu-id="f77cc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f77cc-136">RELATED LINKS</span></span>
