---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b97a8502ff692911812c37d7f1af9d1ce1b33dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959146"
---
# <span data-ttu-id="2e2d3-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e2d3-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="2e2d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2d3-103">Publikuje zmiany z gałęzi Git do bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="2e2d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2e2d3-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e2d3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2e2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="2e2d3-106">Polecenie cmdlet **Publish-AzApiManagementTenantGitConfiguration** publikuje zmiany z gałęzi Git do bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="2e2d3-107">Możesz również sprawdzić poprawność zmian w rozgałęzieniach Git bez publikowania.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="2e2d3-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2e2d3-108">EXAMPLES</span></span>

### <span data-ttu-id="2e2d3-109">Przykład 1. Wdrażanie zmian Git</span><span class="sxs-lookup"><span data-stu-id="2e2d3-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="2e2d3-110">To polecenie publikuje zmiany z określonej gałęzi w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="2e2d3-111">Przykład 2. Sprawdzanie poprawności zmian Git</span><span class="sxs-lookup"><span data-stu-id="2e2d3-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="2e2d3-112">To polecenie sprawdza poprawność zmian w rozgałęzieniu Git w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="2e2d3-113">Nie powoduje publikowania zmian.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-113">It does not publish changes.</span></span>

## <span data-ttu-id="2e2d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e2d3-114">PARAMETERS</span></span>

### <span data-ttu-id="2e2d3-115">— Gałąź</span><span class="sxs-lookup"><span data-stu-id="2e2d3-115">-Branch</span></span>
<span data-ttu-id="2e2d3-116">Określa nazwę gałęzi Git, z której to polecenie cmdlet wdraża konfigurację w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="2e2d3-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="2e2d3-117">-Context</span></span>
<span data-ttu-id="2e2d3-118">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="2e2d3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e2d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2d3-119">-DefaultProfile</span></span>
<span data-ttu-id="2e2d3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e2d3-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2e2d3-121">-Force</span></span>
<span data-ttu-id="2e2d3-122">Wskazuje, że to polecenie cmdlet usuwa subskrypcje produktów usuniętych w tej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="2e2d3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e2d3-123">-PassThru</span></span>
<span data-ttu-id="2e2d3-124">Wskazuje, że to polecenie cmdlet zwraca **obiekt PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="2e2d3-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="2e2d3-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="2e2d3-125">-ValidateOnly</span></span>
<span data-ttu-id="2e2d3-126">Wskazuje, że to polecenie cmdlet sprawdza poprawność zmian w określonej gałęzi Git.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="2e2d3-127">Nie jest publikowana w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="2e2d3-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e2d3-128">-Confirm</span></span>
<span data-ttu-id="2e2d3-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e2d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e2d3-130">-WhatIf</span></span>
<span data-ttu-id="2e2d3-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e2d3-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e2d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2d3-133">CommonParameters</span></span>
<span data-ttu-id="2e2d3-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2d3-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e2d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2d3-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e2d3-136">INPUTS</span></span>

### <span data-ttu-id="2e2d3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e2d3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e2d3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2e2d3-138">System.String</span></span>

### <span data-ttu-id="2e2d3-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="2e2d3-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2e2d3-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e2d3-140">OUTPUTS</span></span>

### <span data-ttu-id="2e2d3-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="2e2d3-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="2e2d3-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2e2d3-142">NOTES</span></span>

## <span data-ttu-id="2e2d3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e2d3-143">RELATED LINKS</span></span>

[<span data-ttu-id="2e2d3-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e2d3-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


