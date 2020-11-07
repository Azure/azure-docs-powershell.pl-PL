---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707088"
---
# <span data-ttu-id="3ebe1-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ebe1-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="3ebe1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ebe1-102">SYNOPSIS</span></span>
<span data-ttu-id="3ebe1-103">Pobiera serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="3ebe1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ebe1-104">SYNTAX</span></span>

### <span data-ttu-id="3ebe1-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ebe1-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ebe1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ebe1-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ebe1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3ebe1-107">DESCRIPTION</span></span>
<span data-ttu-id="3ebe1-108">Polecenie cmdlet **Get-AzApiManagementAuthorizationServer** pobiera wszystkie serwery autoryzacji zarządzania API platformy Azure lub określone serwery autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="3ebe1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ebe1-109">EXAMPLES</span></span>

### <span data-ttu-id="3ebe1-110">Przykład 1: pobieranie wszystkich serwerów autoryzacji</span><span class="sxs-lookup"><span data-stu-id="3ebe1-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="3ebe1-111">To polecenie pobiera wszystkie serwery autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="3ebe1-112">Przykład 2: uzyskiwanie określonego serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="3ebe1-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="3ebe1-113">To polecenie pobiera określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="3ebe1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ebe1-114">PARAMETERS</span></span>

### <span data-ttu-id="3ebe1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="3ebe1-115">-Context</span></span>

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

### <span data-ttu-id="3ebe1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ebe1-116">-DefaultProfile</span></span>
<span data-ttu-id="3ebe1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ebe1-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ebe1-118">-ResourceId</span></span>
<span data-ttu-id="3ebe1-119">Identyfikator zasobu ARM serwera autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="3ebe1-120">Jeśli zostanie określona, spróbuje znaleźć serwer autoryzacji według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="3ebe1-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-121">This parameter is required.</span></span>

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

### <span data-ttu-id="3ebe1-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="3ebe1-122">-ServerId</span></span>
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

### <span data-ttu-id="3ebe1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ebe1-123">CommonParameters</span></span>
<span data-ttu-id="3ebe1-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ebe1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ebe1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ebe1-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ebe1-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ebe1-126">INPUTS</span></span>

### <span data-ttu-id="3ebe1-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ebe1-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ebe1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3ebe1-128">System.String</span></span>

## <span data-ttu-id="3ebe1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ebe1-129">OUTPUTS</span></span>

### <span data-ttu-id="3ebe1-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ebe1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="3ebe1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ebe1-131">NOTES</span></span>

## <span data-ttu-id="3ebe1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ebe1-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ebe1-133">Nowe — AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ebe1-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="3ebe1-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ebe1-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="3ebe1-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ebe1-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)

