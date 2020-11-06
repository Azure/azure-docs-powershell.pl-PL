---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548444"
---
# <span data-ttu-id="269fb-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="269fb-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="269fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="269fb-102">SYNOPSIS</span></span>
<span data-ttu-id="269fb-103">Pobiera serwer autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="269fb-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="269fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="269fb-104">SYNTAX</span></span>

### <span data-ttu-id="269fb-105">Pobieranie wszystkich serwerów autoryzacji (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="269fb-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="269fb-106">Pobierz według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="269fb-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="269fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="269fb-107">DESCRIPTION</span></span>
<span data-ttu-id="269fb-108">Polecenie cmdlet **Get-AzureRmApiManagementAuthorizationServer** pobiera wszystkie serwery autoryzacji zarządzania API platformy Azure lub określone serwery autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="269fb-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="269fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="269fb-109">EXAMPLES</span></span>

### <span data-ttu-id="269fb-110">Przykład 1: pobieranie wszystkich serwerów autoryzacji</span><span class="sxs-lookup"><span data-stu-id="269fb-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="269fb-111">To polecenie pobiera wszystkie serwery autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="269fb-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="269fb-112">Przykład 2: uzyskiwanie określonego serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="269fb-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="269fb-113">To polecenie pobiera określony serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="269fb-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="269fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="269fb-114">PARAMETERS</span></span>

### <span data-ttu-id="269fb-115">-Context</span><span class="sxs-lookup"><span data-stu-id="269fb-115">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="269fb-116">-ServerId</span><span class="sxs-lookup"><span data-stu-id="269fb-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="269fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="269fb-117">-DefaultProfile</span></span>
<span data-ttu-id="269fb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="269fb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="269fb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269fb-119">CommonParameters</span></span>
<span data-ttu-id="269fb-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="269fb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269fb-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="269fb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269fb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="269fb-122">INPUTS</span></span>

## <span data-ttu-id="269fb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="269fb-123">OUTPUTS</span></span>

### <span data-ttu-id="269fb-124">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="269fb-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="269fb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="269fb-125">NOTES</span></span>

## <span data-ttu-id="269fb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="269fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="269fb-127">Nowe — AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="269fb-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="269fb-128">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="269fb-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="269fb-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="269fb-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


