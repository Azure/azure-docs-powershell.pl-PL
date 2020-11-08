---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054230"
---
# <span data-ttu-id="08fb3-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="08fb3-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="08fb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="08fb3-103">Usuwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="08fb3-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="08fb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08fb3-104">SYNTAX</span></span>

### <span data-ttu-id="08fb3-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="08fb3-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="08fb3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="08fb3-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08fb3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08fb3-107">DESCRIPTION</span></span>
<span data-ttu-id="08fb3-108">Usuwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="08fb3-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="08fb3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08fb3-109">EXAMPLES</span></span>

### <span data-ttu-id="08fb3-110">Przykład 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="08fb3-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="08fb3-111">Usuwa TestUbuntu. test. 1.0.0 z galerii stosów Azure.</span><span class="sxs-lookup"><span data-stu-id="08fb3-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="08fb3-112">Przykład 2: Remove-AzsGalleryItem za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="08fb3-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="08fb3-113">Usuwa TestUbuntu. test. 1.0.0 za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="08fb3-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="08fb3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08fb3-114">PARAMETERS</span></span>

### <span data-ttu-id="08fb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08fb3-115">-DefaultProfile</span></span>
<span data-ttu-id="08fb3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08fb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08fb3-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08fb3-117">-InputObject</span></span>
<span data-ttu-id="08fb3-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="08fb3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="08fb3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08fb3-119">-Name</span></span>
<span data-ttu-id="08fb3-120">Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="08fb3-120">Identity of the gallery item.</span></span>
<span data-ttu-id="08fb3-121">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="08fb3-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08fb3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08fb3-122">-PassThru</span></span>
<span data-ttu-id="08fb3-123">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="08fb3-123">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08fb3-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="08fb3-124">-SubscriptionId</span></span>
<span data-ttu-id="08fb3-125">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08fb3-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="08fb3-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="08fb3-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08fb3-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08fb3-127">-Confirm</span></span>
<span data-ttu-id="08fb3-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08fb3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08fb3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08fb3-129">-WhatIf</span></span>
<span data-ttu-id="08fb3-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08fb3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08fb3-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08fb3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08fb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fb3-132">CommonParameters</span></span>
<span data-ttu-id="08fb3-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08fb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fb3-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08fb3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fb3-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08fb3-135">INPUTS</span></span>

### <span data-ttu-id="08fb3-136">Microsoft. Azure. PowerShell. polecenia cmdlet. Gallery. modele. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="08fb3-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="08fb3-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08fb3-137">OUTPUTS</span></span>

### <span data-ttu-id="08fb3-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08fb3-138">System.Boolean</span></span>



## <span data-ttu-id="08fb3-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08fb3-139">NOTES</span></span>

<span data-ttu-id="08fb3-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="08fb3-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08fb3-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08fb3-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="08fb3-142">INPUTobject <IGalleryIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="08fb3-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08fb3-143">`[GalleryItemName <String>]`: Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="08fb3-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="08fb3-144">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="08fb3-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="08fb3-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="08fb3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08fb3-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08fb3-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="08fb3-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="08fb3-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="08fb3-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08fb3-148">RELATED LINKS</span></span>

