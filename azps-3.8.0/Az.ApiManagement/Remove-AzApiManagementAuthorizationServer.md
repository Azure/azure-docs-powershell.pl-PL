---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94054041"
---
# <span data-ttu-id="99b36-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99b36-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="99b36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99b36-102">SYNOPSIS</span></span>
<span data-ttu-id="99b36-103">Usuwa serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="99b36-103">Removes an authorization server.</span></span>

## <span data-ttu-id="99b36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99b36-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99b36-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99b36-105">DESCRIPTION</span></span>
<span data-ttu-id="99b36-106">Polecenie cmdlet **Remove-AzApiManagementAuthorizationServer** usuwa serwer autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="99b36-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="99b36-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99b36-107">EXAMPLES</span></span>

### <span data-ttu-id="99b36-108">Przykład 1: Usuwanie serwera autoryzacji</span><span class="sxs-lookup"><span data-stu-id="99b36-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="99b36-109">To polecenie powoduje usunięcie określonego serwera autoryzacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="99b36-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="99b36-110">Ponieważ parametr *Force* jest określony, nie jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99b36-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="99b36-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99b36-111">PARAMETERS</span></span>

### <span data-ttu-id="99b36-112">-Context</span><span class="sxs-lookup"><span data-stu-id="99b36-112">-Context</span></span>
<span data-ttu-id="99b36-113">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="99b36-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="99b36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b36-114">-DefaultProfile</span></span>
<span data-ttu-id="99b36-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99b36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b36-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99b36-116">-PassThru</span></span>
<span data-ttu-id="99b36-117">passthru</span><span class="sxs-lookup"><span data-stu-id="99b36-117">passthru</span></span>

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

### <span data-ttu-id="99b36-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="99b36-118">-ServerId</span></span>
<span data-ttu-id="99b36-119">Określa identyfikator serwera autoryzacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="99b36-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="99b36-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99b36-120">-Confirm</span></span>
<span data-ttu-id="99b36-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b36-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b36-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b36-122">-WhatIf</span></span>
<span data-ttu-id="99b36-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b36-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b36-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99b36-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b36-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b36-125">CommonParameters</span></span>
<span data-ttu-id="99b36-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b36-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b36-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99b36-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b36-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b36-128">INPUTS</span></span>

### <span data-ttu-id="99b36-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99b36-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="99b36-130">System. String</span><span class="sxs-lookup"><span data-stu-id="99b36-130">System.String</span></span>

### <span data-ttu-id="99b36-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99b36-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99b36-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99b36-132">OUTPUTS</span></span>

### <span data-ttu-id="99b36-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99b36-133">System.Boolean</span></span>

## <span data-ttu-id="99b36-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99b36-134">NOTES</span></span>

## <span data-ttu-id="99b36-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99b36-135">RELATED LINKS</span></span>

[<span data-ttu-id="99b36-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99b36-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="99b36-137">Nowe — AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99b36-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="99b36-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="99b36-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


