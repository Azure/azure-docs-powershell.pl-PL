---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182363"
---
# <span data-ttu-id="dd5ef-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd5ef-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="dd5ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd5ef-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5ef-103">Publikuje zmiany z gałęzi Git do bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="dd5ef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd5ef-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd5ef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd5ef-105">DESCRIPTION</span></span>
<span data-ttu-id="dd5ef-106">Polecenie cmdlet **Publish-AzApiManagementTenantGitConfiguration** publikuje zmiany z gałęzi Git do bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="dd5ef-107">Możesz również sprawdzić poprawność zmian w rozgałęzieniach Git bez publikowania.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="dd5ef-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd5ef-108">EXAMPLES</span></span>

### <span data-ttu-id="dd5ef-109">Przykład 1. Wdrażanie zmian Git</span><span class="sxs-lookup"><span data-stu-id="dd5ef-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="dd5ef-110">To polecenie publikuje zmiany z określonej gałęzi w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="dd5ef-111">Przykład 2. Sprawdzanie poprawności zmian Git</span><span class="sxs-lookup"><span data-stu-id="dd5ef-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="dd5ef-112">To polecenie sprawdza poprawność zmian w rozgałęzieniu Git w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="dd5ef-113">Nie publikuje on zmian.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-113">It does not publish changes.</span></span>

## <span data-ttu-id="dd5ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd5ef-114">PARAMETERS</span></span>

### <span data-ttu-id="dd5ef-115">— Gałąź</span><span class="sxs-lookup"><span data-stu-id="dd5ef-115">-Branch</span></span>
<span data-ttu-id="dd5ef-116">Określa nazwę gałęzi Git, z której to polecenie cmdlet wdraża konfigurację w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="dd5ef-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="dd5ef-117">-Context</span></span>
<span data-ttu-id="dd5ef-118">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="dd5ef-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dd5ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5ef-119">-DefaultProfile</span></span>
<span data-ttu-id="dd5ef-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd5ef-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="dd5ef-121">-Force</span></span>
<span data-ttu-id="dd5ef-122">Wskazuje, że to polecenie cmdlet usuwa subskrypcje produktów usuniętych w tej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="dd5ef-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd5ef-123">-PassThru</span></span>
<span data-ttu-id="dd5ef-124">Wskazuje, że to polecenie cmdlet zwraca **obiekt PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="dd5ef-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="dd5ef-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="dd5ef-125">-ValidateOnly</span></span>
<span data-ttu-id="dd5ef-126">Wskazuje, że to polecenie cmdlet sprawdza poprawność zmian w określonej gałęzi Git.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="dd5ef-127">Nie jest publikowana w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="dd5ef-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd5ef-128">-Confirm</span></span>
<span data-ttu-id="dd5ef-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5ef-130">-WhatIf</span></span>
<span data-ttu-id="dd5ef-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5ef-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5ef-133">CommonParameters</span></span>
<span data-ttu-id="dd5ef-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5ef-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd5ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5ef-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd5ef-136">INPUTS</span></span>

### <span data-ttu-id="dd5ef-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd5ef-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd5ef-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dd5ef-138">System.String</span></span>

### <span data-ttu-id="dd5ef-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="dd5ef-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd5ef-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd5ef-140">OUTPUTS</span></span>

### <span data-ttu-id="dd5ef-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="dd5ef-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="dd5ef-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd5ef-142">NOTES</span></span>

## <span data-ttu-id="dd5ef-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd5ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="dd5ef-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd5ef-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


