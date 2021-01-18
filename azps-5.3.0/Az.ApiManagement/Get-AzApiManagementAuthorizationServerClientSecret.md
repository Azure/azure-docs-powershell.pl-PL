---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502510"
---
# <span data-ttu-id="171bd-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="171bd-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="171bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="171bd-102">SYNOPSIS</span></span>
<span data-ttu-id="171bd-103">Pobiera klucz tajny klienta serwera autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="171bd-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="171bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="171bd-104">SYNTAX</span></span>

### <span data-ttu-id="171bd-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="171bd-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="171bd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="171bd-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="171bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="171bd-107">DESCRIPTION</span></span>
<span data-ttu-id="171bd-108">Polecenie cmdlet **Get-AzApiManagementAuthorizationServerClientSecret** Pobiera klucz tajny klienta serwera autoryzacji usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="171bd-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="171bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="171bd-109">EXAMPLES</span></span>

### <span data-ttu-id="171bd-110">Przykład 1: uzyskiwanie określonego klucza tajnego klienta serwera autoryzacji według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="171bd-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="171bd-111">To polecenie umożliwia pobieranie określonego klucza tajnego cient serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="171bd-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="171bd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="171bd-112">PARAMETERS</span></span>

### <span data-ttu-id="171bd-113">-Context</span><span class="sxs-lookup"><span data-stu-id="171bd-113">-Context</span></span>
<span data-ttu-id="171bd-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="171bd-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="171bd-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="171bd-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171bd-116">-DefaultProfile</span></span>
<span data-ttu-id="171bd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="171bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="171bd-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="171bd-118">-ResourceId</span></span>
<span data-ttu-id="171bd-119">Identyfikator zasobu ARM serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="171bd-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="171bd-120">Jeśli zostanie określona, spróbuje znaleźć serwer autoryzacji według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="171bd-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="171bd-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="171bd-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="171bd-122">-ServerId</span></span>
<span data-ttu-id="171bd-123">Identyfikator serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="171bd-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="171bd-124">Jeśli to pole jest określone, zostanie znaleziony identyfikator serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="171bd-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="171bd-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="171bd-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171bd-126">CommonParameters</span></span>
<span data-ttu-id="171bd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="171bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171bd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="171bd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171bd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="171bd-129">INPUTS</span></span>

### <span data-ttu-id="171bd-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="171bd-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="171bd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="171bd-131">System.String</span></span>

## <span data-ttu-id="171bd-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="171bd-132">OUTPUTS</span></span>

### <span data-ttu-id="171bd-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="171bd-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="171bd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="171bd-134">NOTES</span></span>

## <span data-ttu-id="171bd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="171bd-135">RELATED LINKS</span></span>
