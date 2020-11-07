---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898634"
---
# <span data-ttu-id="7615e-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7615e-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="7615e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7615e-102">SYNOPSIS</span></span>
<span data-ttu-id="7615e-103">Modyfikuje rolę niestandardową w usłudze Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="7615e-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="7615e-104">Podaj zmodyfikowaną definicję roli jako plik JSON lub jako PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="7615e-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="7615e-105">Najpierw użyj polecenia Get-AzureRmRoleDefinition, aby pobrać rolę niestandardową, którą chcesz zmodyfikować.</span><span class="sxs-lookup"><span data-stu-id="7615e-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="7615e-106">Następnie zmodyfikuj właściwości, które chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="7615e-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="7615e-107">Na koniec Zapisz definicję roli za pomocą tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="7615e-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7615e-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7615e-108">SYNTAX</span></span>

### <span data-ttu-id="7615e-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7615e-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7615e-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7615e-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7615e-111">Opis</span><span class="sxs-lookup"><span data-stu-id="7615e-111">DESCRIPTION</span></span>
<span data-ttu-id="7615e-112">Polecenie cmdlet Set-AzureRmRoleDefinition aktualizuje istniejącą rolę niestandardową w kontroli dostępu na platformie Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="7615e-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="7615e-113">Wprowadź zaktualizowaną definicję roli jako dane wejściowe polecenia jako plik JSON lub obiekt PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="7615e-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="7615e-114">Definicja roli zaktualizowanej roli niestandardowej musi zawierać identyfikator i wszystkie inne wymagane właściwości roli, nawet jeśli nie zostały zaktualizowane: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="7615e-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="7615e-115">Nienaruszone, akcje dataNotDataActions są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="7615e-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="7615e-116">Poniżej przedstawiono przykładowy kod JSON zaktualizowanej definicji ról dla Set-AzureRmRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e"; "nazwa": "zaktualizowana rola", "opis": "może monitorować wszystkie zasoby i uruchamiać i ponownie uruchamiać maszyny wirtualne", "akcje": \[ " */Read", "Microsoft. ClassicCompute/virtualmachines/Action", "Microsoft. ClassicCompute/virtualmachines/Start/Action" \] ; "zanaruszone": \[ "* /Write" \] ; "akcje danych": \[ "Microsoft. Storage/storageAccounts/blobServices/Containers/BLOB/Read", "NotDataActions": "Microsoft. Storage/storageAccounts/blobServices/Containers \] \[ /BLOB/Write", "AssignableScopes" \] : \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="7615e-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="7615e-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7615e-117">EXAMPLES</span></span>

### <span data-ttu-id="7615e-118">Aktualizowanie przy użyciu PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="7615e-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="7615e-119">Tworzenie przy użyciu pliku JSON</span><span class="sxs-lookup"><span data-stu-id="7615e-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="7615e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7615e-120">PARAMETERS</span></span>

### <span data-ttu-id="7615e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7615e-121">-DefaultProfile</span></span>
<span data-ttu-id="7615e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7615e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7615e-123">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="7615e-123">-InputFile</span></span>
<span data-ttu-id="7615e-124">Nazwa pliku zawierającego pojedynczą definicję roli JSON do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7615e-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="7615e-125">Uwzględnij tylko właściwości, które mają zostać zaktualizowane w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="7615e-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="7615e-126">Właściwość ID jest wymagana.</span><span class="sxs-lookup"><span data-stu-id="7615e-126">Id property is Required.</span></span>

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

### <span data-ttu-id="7615e-127">-Rola</span><span class="sxs-lookup"><span data-stu-id="7615e-127">-Role</span></span>
<span data-ttu-id="7615e-128">Obiekt definicji roli do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="7615e-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="7615e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7615e-129">CommonParameters</span></span>
<span data-ttu-id="7615e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7615e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7615e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7615e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7615e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7615e-132">INPUTS</span></span>

### <span data-ttu-id="7615e-133">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7615e-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="7615e-134">Parametry: role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7615e-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="7615e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7615e-135">OUTPUTS</span></span>

### <span data-ttu-id="7615e-136">Microsoft. Azure. Commands. resources. models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7615e-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7615e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7615e-137">NOTES</span></span>
<span data-ttu-id="7615e-138">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="7615e-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7615e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7615e-139">RELATED LINKS</span></span>

[<span data-ttu-id="7615e-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="7615e-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="7615e-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7615e-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="7615e-142">Nowe — AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7615e-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="7615e-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7615e-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

