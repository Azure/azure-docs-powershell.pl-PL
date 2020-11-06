---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524721"
---
# <span data-ttu-id="b85dd-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b85dd-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="b85dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b85dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b85dd-103">Usuwa serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b85dd-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b85dd-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b85dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b85dd-106">Polecenie cmdlet **Remove-AzureRmApiManagementAuthorizationServer** usuwa serwer autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="b85dd-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="b85dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b85dd-107">EXAMPLES</span></span>

## <span data-ttu-id="b85dd-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b85dd-108">PARAMETERS</span></span>

### <span data-ttu-id="b85dd-109">-Context</span><span class="sxs-lookup"><span data-stu-id="b85dd-109">-Context</span></span>
<span data-ttu-id="b85dd-110">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b85dd-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b85dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85dd-111">-DefaultProfile</span></span>
<span data-ttu-id="b85dd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b85dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85dd-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b85dd-113">-PassThru</span></span>
<span data-ttu-id="b85dd-114">passthru</span><span class="sxs-lookup"><span data-stu-id="b85dd-114">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85dd-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b85dd-115">-ServerId</span></span>
<span data-ttu-id="b85dd-116">Określa identyfikator serwera autoryzacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b85dd-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="b85dd-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b85dd-117">-Confirm</span></span>
<span data-ttu-id="b85dd-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85dd-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85dd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85dd-119">-WhatIf</span></span>
<span data-ttu-id="b85dd-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b85dd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85dd-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b85dd-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85dd-122">CommonParameters</span></span>
<span data-ttu-id="b85dd-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85dd-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85dd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85dd-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b85dd-125">INPUTS</span></span>

### <span data-ttu-id="b85dd-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b85dd-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b85dd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b85dd-127">System.String</span></span>

### <span data-ttu-id="b85dd-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b85dd-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b85dd-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b85dd-129">OUTPUTS</span></span>

### <span data-ttu-id="b85dd-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b85dd-130">System.Boolean</span></span>

## <span data-ttu-id="b85dd-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b85dd-131">NOTES</span></span>

## <span data-ttu-id="b85dd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b85dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="b85dd-133">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b85dd-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="b85dd-134">Nowe — AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b85dd-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="b85dd-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b85dd-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


