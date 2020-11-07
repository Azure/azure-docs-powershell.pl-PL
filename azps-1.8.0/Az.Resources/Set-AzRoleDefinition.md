---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 0ea0c0345bc57a7b1bd5c0c4cf67d6bd400542be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708268"
---
# <span data-ttu-id="e507b-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e507b-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="e507b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e507b-102">SYNOPSIS</span></span>
<span data-ttu-id="e507b-103">Modyfikuje rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e507b-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="e507b-104">Podaj zmodyfikowaną definicję roli jako plik JSON lub jako PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="e507b-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="e507b-105">Najpierw użyj polecenia Get-AzRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="e507b-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="e507b-106">Następnie zmodyfikuj właściwości, które chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="e507b-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="e507b-107">Na koniec Zapisz definicję roli za pomocą tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="e507b-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="e507b-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e507b-108">SYNTAX</span></span>

### <span data-ttu-id="e507b-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e507b-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e507b-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e507b-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e507b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="e507b-111">DESCRIPTION</span></span>
<span data-ttu-id="e507b-112">Polecenie cmdlet Set-AzRoleDefinition aktualizuje istniejącą rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="e507b-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="e507b-113">Wprowadź zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="e507b-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="e507b-114">Definicja roli zaktualizowanej roli niestandardowej musi zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie zostały zaktualizowane: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="e507b-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="e507b-115">Nienaruszone, akcje dataNotDataActions są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="e507b-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="e507b-116">Poniżej przedstawiono przykładowy kod JSON zaktualizowanej definicji ról dla Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e"; "nazwa": "zaktualizowana rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="e507b-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="e507b-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e507b-117">EXAMPLES</span></span>

### <span data-ttu-id="e507b-118">Aktualizowanie przy użyciu PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="e507b-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="e507b-119">Tworzenie przy użyciu pliku JSON</span><span class="sxs-lookup"><span data-stu-id="e507b-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="e507b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e507b-120">PARAMETERS</span></span>

### <span data-ttu-id="e507b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e507b-121">-DefaultProfile</span></span>
<span data-ttu-id="e507b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e507b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e507b-123">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="e507b-123">-InputFile</span></span>
<span data-ttu-id="e507b-124">Nazwa pliku zawierającego pojedynczą definicję roli JSON do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="e507b-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="e507b-125">Uwzględnij tylko właściwości, które mają zostać zaktualizowane w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="e507b-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="e507b-126">Właściwość ID jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="e507b-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e507b-127">-Rola</span><span class="sxs-lookup"><span data-stu-id="e507b-127">-Role</span></span>
<span data-ttu-id="e507b-128">Obiekt definicji roli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="e507b-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e507b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e507b-129">CommonParameters</span></span>
<span data-ttu-id="e507b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e507b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e507b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e507b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e507b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e507b-132">INPUTS</span></span>

### <span data-ttu-id="e507b-133">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e507b-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="e507b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e507b-134">OUTPUTS</span></span>

### <span data-ttu-id="e507b-135">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e507b-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="e507b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e507b-136">NOTES</span></span>
<span data-ttu-id="e507b-137">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="e507b-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e507b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e507b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e507b-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="e507b-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="e507b-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e507b-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="e507b-141">Nowe — AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e507b-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="e507b-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e507b-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

