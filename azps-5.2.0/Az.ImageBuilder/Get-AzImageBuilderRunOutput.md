---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337057"
---
# <span data-ttu-id="f128e-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="f128e-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="f128e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f128e-102">SYNOPSIS</span></span>
<span data-ttu-id="f128e-103">Uzyskiwanie określonego wyjścia uruchomienia dla określonego zasobu szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="f128e-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="f128e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f128e-104">SYNTAX</span></span>

### <span data-ttu-id="f128e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f128e-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f128e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f128e-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f128e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f128e-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f128e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f128e-108">DESCRIPTION</span></span>
<span data-ttu-id="f128e-109">Uzyskiwanie określonego wyjścia uruchomienia dla określonego zasobu szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="f128e-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="f128e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f128e-110">EXAMPLES</span></span>

### <span data-ttu-id="f128e-111">Przykład 1: wyświetlanie wszystkich wyników uruchamiania na podstawie szablonu</span><span class="sxs-lookup"><span data-stu-id="f128e-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="f128e-112">To polecenie wyświetla wszystkie wyniki uruchamiania pod szablonem.</span><span class="sxs-lookup"><span data-stu-id="f128e-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="f128e-113">Przykład 2: uzyskiwanie wyniku uruchomienia pod szablonem</span><span class="sxs-lookup"><span data-stu-id="f128e-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="f128e-114">To polecenie uzyskuje wynik uruchomienia pod szablonem.</span><span class="sxs-lookup"><span data-stu-id="f128e-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="f128e-115">Przykład 3: uzyskiwanie wyniku uruchomienia pod szablonem</span><span class="sxs-lookup"><span data-stu-id="f128e-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="f128e-116">To polecenie uzyskuje wynik uruchomienia pod szablonem.</span><span class="sxs-lookup"><span data-stu-id="f128e-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="f128e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f128e-117">PARAMETERS</span></span>

### <span data-ttu-id="f128e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f128e-118">-DefaultProfile</span></span>
<span data-ttu-id="f128e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f128e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f128e-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="f128e-120">-ImageTemplateName</span></span>
<span data-ttu-id="f128e-121">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="f128e-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f128e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f128e-122">-InputObject</span></span>
<span data-ttu-id="f128e-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f128e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f128e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f128e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f128e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f128e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f128e-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="f128e-126">-RunOutputName</span></span>
<span data-ttu-id="f128e-127">Nazwa wyjścia do uruchamiania</span><span class="sxs-lookup"><span data-stu-id="f128e-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f128e-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f128e-128">-SubscriptionId</span></span>
<span data-ttu-id="f128e-129">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f128e-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f128e-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f128e-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f128e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f128e-131">CommonParameters</span></span>
<span data-ttu-id="f128e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f128e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f128e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f128e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f128e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f128e-134">INPUTS</span></span>

### <span data-ttu-id="f128e-135">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="f128e-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="f128e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f128e-136">OUTPUTS</span></span>

### <span data-ttu-id="f128e-137">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="f128e-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="f128e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f128e-138">NOTES</span></span>

<span data-ttu-id="f128e-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f128e-139">ALIASES</span></span>

<span data-ttu-id="f128e-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f128e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f128e-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f128e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f128e-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f128e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f128e-143">INPUTobject <IImageBuilderIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f128e-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f128e-144">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f128e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f128e-145">`[ImageTemplateName <String>]`: Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="f128e-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="f128e-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f128e-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f128e-147">`[RunOutputName <String>]`: Nazwa wyjścia do uruchomienia</span><span class="sxs-lookup"><span data-stu-id="f128e-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="f128e-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f128e-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f128e-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f128e-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f128e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f128e-150">RELATED LINKS</span></span>

