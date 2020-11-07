---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 71f4960dce883b809d9ee9c5bc7011d8ab04c5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706982"
---
# <span data-ttu-id="26065-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="26065-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="26065-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26065-102">SYNOPSIS</span></span>
<span data-ttu-id="26065-103">Generuje token dostępu współdzielonego dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="26065-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="26065-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26065-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26065-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26065-105">DESCRIPTION</span></span>
<span data-ttu-id="26065-106">Polecenie cmdlet **New-AzApiManagementUserToken** generuje token dostępu współużytkowanego dla określonego użytkownika</span><span class="sxs-lookup"><span data-stu-id="26065-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="26065-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26065-107">EXAMPLES</span></span>

### <span data-ttu-id="26065-108">Przykład 1. Wygeneruj token dostępu współdzielonego dla użytkownika git</span><span class="sxs-lookup"><span data-stu-id="26065-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="26065-109">Ten skrypt uzyskuje użytkownika git skonfigurowanego w usłudze ApiManagement i generuje token dostępu udostępnionego przy użyciu klucza podstawowego ważnego na 8 godzin.</span><span class="sxs-lookup"><span data-stu-id="26065-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="26065-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26065-110">PARAMETERS</span></span>

### <span data-ttu-id="26065-111">-Context</span><span class="sxs-lookup"><span data-stu-id="26065-111">-Context</span></span>
<span data-ttu-id="26065-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="26065-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="26065-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="26065-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26065-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26065-114">-DefaultProfile</span></span>
<span data-ttu-id="26065-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26065-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26065-116">-Wygasanie</span><span class="sxs-lookup"><span data-stu-id="26065-116">-Expiry</span></span>
<span data-ttu-id="26065-117">Wygaśnięcie tokenu.</span><span class="sxs-lookup"><span data-stu-id="26065-117">Expiry of the Token.</span></span>
<span data-ttu-id="26065-118">Jeśli nie określono tego pola, token zostanie utworzony po upływie 8 godzin.</span><span class="sxs-lookup"><span data-stu-id="26065-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="26065-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="26065-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26065-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="26065-120">-KeyType</span></span>
<span data-ttu-id="26065-121">Klucz użytkownika, który ma być używany podczas generowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="26065-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="26065-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="26065-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26065-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="26065-123">-UserId</span></span>
<span data-ttu-id="26065-124">Identyfikator istniejącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="26065-124">Identifier of existing user.</span></span>
<span data-ttu-id="26065-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="26065-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26065-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26065-126">CommonParameters</span></span>
<span data-ttu-id="26065-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26065-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26065-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26065-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26065-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26065-129">INPUTS</span></span>

### <span data-ttu-id="26065-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26065-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26065-131">System. String</span><span class="sxs-lookup"><span data-stu-id="26065-131">System.String</span></span>

### <span data-ttu-id="26065-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="26065-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="26065-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26065-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="26065-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26065-134">OUTPUTS</span></span>

### <span data-ttu-id="26065-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="26065-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="26065-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26065-136">NOTES</span></span>

## <span data-ttu-id="26065-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26065-137">RELATED LINKS</span></span>
