---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051170"
---
# <span data-ttu-id="1b87f-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b87f-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="1b87f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b87f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b87f-103">Publikuje zmiany z gałęzi Git w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="1b87f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b87f-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b87f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b87f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b87f-106">Polecenie cmdlet **Publish-AzApiManagementTenantGitConfiguration** publikuje zmiany z gałęzi Git w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="1b87f-107">Możesz również sprawdzić poprawność zmian w gałęzi git bez publikowania.</span><span class="sxs-lookup"><span data-stu-id="1b87f-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="1b87f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b87f-108">EXAMPLES</span></span>

### <span data-ttu-id="1b87f-109">Przykład 1: wdrażanie zmian git</span><span class="sxs-lookup"><span data-stu-id="1b87f-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="1b87f-110">To polecenie umożliwia publikowanie zmian z określonej gałęzi do bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="1b87f-111">Przykład 2: sprawdzanie poprawności zmian git</span><span class="sxs-lookup"><span data-stu-id="1b87f-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="1b87f-112">To polecenie sprawdza poprawność zmian w gałęzi usługi git dla bazy danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="1b87f-113">Zmiany nie są publikowane.</span><span class="sxs-lookup"><span data-stu-id="1b87f-113">It does not publish changes.</span></span>

## <span data-ttu-id="1b87f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b87f-114">PARAMETERS</span></span>

### <span data-ttu-id="1b87f-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="1b87f-115">-Branch</span></span>
<span data-ttu-id="1b87f-116">Określa nazwę gałęzi git, z której to polecenie cmdlet wdraża konfigurację w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="1b87f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="1b87f-117">-Context</span></span>
<span data-ttu-id="1b87f-118">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1b87f-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b87f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b87f-119">-DefaultProfile</span></span>
<span data-ttu-id="1b87f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b87f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b87f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1b87f-121">-Force</span></span>
<span data-ttu-id="1b87f-122">Wskazuje, że to polecenie cmdlet usunie subskrypcje produktów, które zostały usunięte w tej aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="1b87f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b87f-123">-PassThru</span></span>
<span data-ttu-id="1b87f-124">Wskazuje, że to polecenie cmdlet zwraca obiekt **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="1b87f-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="1b87f-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="1b87f-125">-ValidateOnly</span></span>
<span data-ttu-id="1b87f-126">Wskazuje, że to polecenie cmdlet sprawdza poprawność zmian w określonej gałęzi git.</span><span class="sxs-lookup"><span data-stu-id="1b87f-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="1b87f-127">Nie jest on publikowany w bazie danych konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1b87f-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="1b87f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b87f-128">-Confirm</span></span>
<span data-ttu-id="1b87f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b87f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b87f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b87f-130">-WhatIf</span></span>
<span data-ttu-id="1b87f-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b87f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b87f-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b87f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b87f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b87f-133">CommonParameters</span></span>
<span data-ttu-id="1b87f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b87f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b87f-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b87f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b87f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b87f-136">INPUTS</span></span>

### <span data-ttu-id="1b87f-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1b87f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1b87f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1b87f-138">System.String</span></span>

### <span data-ttu-id="1b87f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b87f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b87f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b87f-140">OUTPUTS</span></span>

### <span data-ttu-id="1b87f-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="1b87f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="1b87f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b87f-142">NOTES</span></span>

## <span data-ttu-id="1b87f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b87f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1b87f-144">Zapisz — AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b87f-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


