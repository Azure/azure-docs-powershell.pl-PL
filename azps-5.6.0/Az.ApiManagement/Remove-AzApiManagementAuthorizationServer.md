---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973002"
---
# <span data-ttu-id="fe3cf-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="fe3cf-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="fe3cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3cf-103">Usuwa serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-103">Removes an authorization server.</span></span>

## <span data-ttu-id="fe3cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe3cf-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3cf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe3cf-105">DESCRIPTION</span></span>
<span data-ttu-id="fe3cf-106">Polecenie **cmdlet Remove-AzApiManagementAuthorizationServer** usuwa serwer autoryzacji usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="fe3cf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe3cf-107">EXAMPLES</span></span>

### <span data-ttu-id="fe3cf-108">Przykład 1. Usuwanie serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="fe3cf-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="fe3cf-109">To polecenie usuwa określony serwer autoryzacji zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="fe3cf-110">Parametr *Force jest* określony, dlatego potwierdzenie nie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="fe3cf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3cf-111">PARAMETERS</span></span>

### <span data-ttu-id="fe3cf-112">— kontekst</span><span class="sxs-lookup"><span data-stu-id="fe3cf-112">-Context</span></span>
<span data-ttu-id="fe3cf-113">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="fe3cf-113">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3cf-114">-DefaultProfile</span></span>
<span data-ttu-id="fe3cf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe3cf-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe3cf-116">-PassThru</span></span>
<span data-ttu-id="fe3cf-117">passthru</span><span class="sxs-lookup"><span data-stu-id="fe3cf-117">passthru</span></span>

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

### <span data-ttu-id="fe3cf-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="fe3cf-118">-ServerId</span></span>
<span data-ttu-id="fe3cf-119">Określa identyfikator serwera autoryzacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="fe3cf-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe3cf-120">-Confirm</span></span>
<span data-ttu-id="fe3cf-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3cf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3cf-122">-WhatIf</span></span>
<span data-ttu-id="fe3cf-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3cf-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3cf-125">CommonParameters</span></span>
<span data-ttu-id="fe3cf-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3cf-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe3cf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3cf-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe3cf-128">INPUTS</span></span>

### <span data-ttu-id="fe3cf-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe3cf-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe3cf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fe3cf-130">System.String</span></span>

### <span data-ttu-id="fe3cf-131">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="fe3cf-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe3cf-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe3cf-132">OUTPUTS</span></span>

### <span data-ttu-id="fe3cf-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe3cf-133">System.Boolean</span></span>

## <span data-ttu-id="fe3cf-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe3cf-134">NOTES</span></span>

## <span data-ttu-id="fe3cf-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe3cf-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe3cf-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="fe3cf-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="fe3cf-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="fe3cf-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="fe3cf-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="fe3cf-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


