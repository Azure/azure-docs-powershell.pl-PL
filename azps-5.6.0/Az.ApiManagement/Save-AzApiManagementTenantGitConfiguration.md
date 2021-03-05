---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: eb865535fcb4ee49b834e923fcf3f319ff5de074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965521"
---
# <span data-ttu-id="16ef8-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="16ef8-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="16ef8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="16ef8-103">Zapisuje zmiany przez utworzenie zatwierdzenia dla bieżącej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="16ef8-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="16ef8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16ef8-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ef8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="16ef8-105">DESCRIPTION</span></span>
<span data-ttu-id="16ef8-106">Polecenie cmdlet **Save-AzApiManagementTenantGitConfiguration** zapisuje zmiany, tworząc zatwierdzenie zawierające bieżącą migawkę konfiguracji w gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="16ef8-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="16ef8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16ef8-107">EXAMPLES</span></span>

### <span data-ttu-id="16ef8-108">Przykład 1. Zapisywanie zmian w konfiguracji</span><span class="sxs-lookup"><span data-stu-id="16ef8-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="16ef8-109">To polecenie zapisuje zmiany, tworząc zatwierdzenie za pomocą bieżącej migawki konfiguracji w określonej gałęzi w repozytorium.</span><span class="sxs-lookup"><span data-stu-id="16ef8-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="16ef8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16ef8-110">PARAMETERS</span></span>

### <span data-ttu-id="16ef8-111">— Gałąź</span><span class="sxs-lookup"><span data-stu-id="16ef8-111">-Branch</span></span>
<span data-ttu-id="16ef8-112">Określa nazwę gałęzi Git, w której ma na celu zatwierdzenie bieżącej migawki konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="16ef8-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="16ef8-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="16ef8-113">-Context</span></span>
<span data-ttu-id="16ef8-114">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="16ef8-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="16ef8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ef8-115">-DefaultProfile</span></span>
<span data-ttu-id="16ef8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16ef8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ef8-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="16ef8-117">-Force</span></span>
<span data-ttu-id="16ef8-118">Określa, że to polecenie cmdlet powoduje zatwierdzenie bieżącej bazy danych konfiguracji do repozytorium Git, nawet jeśli repozytorium Git zawiera nowsze zmiany, które zostaną zastąpione.</span><span class="sxs-lookup"><span data-stu-id="16ef8-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="16ef8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16ef8-119">-PassThru</span></span>
<span data-ttu-id="16ef8-120">Wskazuje, że to polecenie cmdlet zwraca **obiekt PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="16ef8-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="16ef8-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16ef8-121">-Confirm</span></span>
<span data-ttu-id="16ef8-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16ef8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ef8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ef8-123">-WhatIf</span></span>
<span data-ttu-id="16ef8-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16ef8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ef8-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16ef8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ef8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ef8-126">CommonParameters</span></span>
<span data-ttu-id="16ef8-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ef8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ef8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16ef8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ef8-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16ef8-129">INPUTS</span></span>

### <span data-ttu-id="16ef8-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="16ef8-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16ef8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="16ef8-131">System.String</span></span>

### <span data-ttu-id="16ef8-132">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="16ef8-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="16ef8-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16ef8-133">OUTPUTS</span></span>

### <span data-ttu-id="16ef8-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="16ef8-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="16ef8-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16ef8-135">NOTES</span></span>

## <span data-ttu-id="16ef8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16ef8-136">RELATED LINKS</span></span>

[<span data-ttu-id="16ef8-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="16ef8-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


