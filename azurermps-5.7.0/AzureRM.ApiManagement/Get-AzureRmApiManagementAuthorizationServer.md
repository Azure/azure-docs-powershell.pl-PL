---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717758"
---
# <span data-ttu-id="b7bb2-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b7bb2-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="b7bb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b7bb2-103">Pobiera serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7bb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7bb2-104">SYNTAX</span></span>

### <span data-ttu-id="b7bb2-105">GetAllAuthorizationServers (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7bb2-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="b7bb2-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7bb2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b7bb2-107">DESCRIPTION</span></span>
<span data-ttu-id="b7bb2-108">Polecenie cmdlet **Get-AzureRmApiManagementAuthorizationServer** pobiera wszystkie serwery autoryzacji zarządzania API platformy Azure lub określone serwery autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="b7bb2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="b7bb2-110">Przykład 1: pobieranie wszystkich serwerów autoryzacji</span><span class="sxs-lookup"><span data-stu-id="b7bb2-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="b7bb2-111">To polecenie pobiera wszystkie serwery autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="b7bb2-112">Przykład 2: uzyskiwanie określonego serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="b7bb2-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="b7bb2-113">To polecenie pobiera określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="b7bb2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7bb2-114">PARAMETERS</span></span>

### <span data-ttu-id="b7bb2-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b7bb2-115">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7bb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7bb2-116">-DefaultProfile</span></span>
<span data-ttu-id="b7bb2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b7bb2-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b7bb2-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7bb2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7bb2-119">CommonParameters</span></span>
<span data-ttu-id="b7bb2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7bb2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7bb2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7bb2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7bb2-122">INPUTS</span></span>

### <span data-ttu-id="b7bb2-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b7bb2-123">None</span></span>
<span data-ttu-id="b7bb2-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7bb2-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7bb2-125">OUTPUTS</span></span>

### <span data-ttu-id="b7bb2-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="b7bb2-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="b7bb2-127">Szczegóły serwera autoryzacji w danej usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="b7bb2-128">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="b7bb2-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="b7bb2-129">Lista serwerów autoryzacji w danej usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="b7bb2-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7bb2-130">NOTES</span></span>

## <span data-ttu-id="b7bb2-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7bb2-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7bb2-132">Nowe — AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b7bb2-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="b7bb2-133">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b7bb2-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="b7bb2-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b7bb2-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


