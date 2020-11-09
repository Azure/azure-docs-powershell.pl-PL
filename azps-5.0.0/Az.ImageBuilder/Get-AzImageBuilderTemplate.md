---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304032"
---
# <span data-ttu-id="3a57f-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="3a57f-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="3a57f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a57f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a57f-103">Uzyskiwanie informacji na temat szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3a57f-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="3a57f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a57f-104">SYNTAX</span></span>

### <span data-ttu-id="3a57f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3a57f-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a57f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3a57f-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a57f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a57f-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a57f-108">List1</span><span class="sxs-lookup"><span data-stu-id="3a57f-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3a57f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3a57f-109">DESCRIPTION</span></span>
<span data-ttu-id="3a57f-110">Uzyskiwanie informacji na temat szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3a57f-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="3a57f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a57f-111">EXAMPLES</span></span>

### <span data-ttu-id="3a57f-112">Przykład 1: wyświetlanie wszystkich szablonów w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="3a57f-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="3a57f-113">To polecenie wyświetla listę wszystkich szablonów objętych abonamentem.</span><span class="sxs-lookup"><span data-stu-id="3a57f-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="3a57f-114">Przykład 2: wyświetlanie wszystkich szablonów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="3a57f-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="3a57f-115">To polecenie wyświetla listę wszystkich szablonów znajdujących się w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a57f-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="3a57f-116">Przykład 3: uzyskiwanie szablonu pod grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="3a57f-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="3a57f-117">To polecenie pobiera szablon pod grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a57f-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="3a57f-118">Przykład 4: uzyskiwanie szablonu pod grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="3a57f-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="3a57f-119">To polecenie pobiera szablon pod grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a57f-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="3a57f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a57f-120">PARAMETERS</span></span>

### <span data-ttu-id="3a57f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a57f-121">-DefaultProfile</span></span>
<span data-ttu-id="3a57f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a57f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a57f-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="3a57f-123">-ImageTemplateName</span></span>
<span data-ttu-id="3a57f-124">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="3a57f-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a57f-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a57f-125">-InputObject</span></span>
<span data-ttu-id="3a57f-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3a57f-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a57f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a57f-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a57f-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a57f-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a57f-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3a57f-129">-SubscriptionId</span></span>
<span data-ttu-id="3a57f-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a57f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a57f-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3a57f-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a57f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a57f-132">CommonParameters</span></span>
<span data-ttu-id="3a57f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a57f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a57f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a57f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a57f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a57f-135">INPUTS</span></span>

### <span data-ttu-id="3a57f-136">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="3a57f-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="3a57f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a57f-137">OUTPUTS</span></span>

### <span data-ttu-id="3a57f-138">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="3a57f-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="3a57f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a57f-139">NOTES</span></span>

<span data-ttu-id="3a57f-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3a57f-140">ALIASES</span></span>

<span data-ttu-id="3a57f-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a57f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a57f-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a57f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a57f-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a57f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a57f-144">INPUTobject <IImageBuilderIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3a57f-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a57f-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3a57f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a57f-146">`[ImageTemplateName <String>]`: Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="3a57f-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="3a57f-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a57f-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3a57f-148">`[RunOutputName <String>]`: Nazwa wyjścia do uruchomienia</span><span class="sxs-lookup"><span data-stu-id="3a57f-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="3a57f-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a57f-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3a57f-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3a57f-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3a57f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a57f-151">RELATED LINKS</span></span>

