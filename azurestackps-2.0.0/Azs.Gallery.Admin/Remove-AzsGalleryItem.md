---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891725"
---
# <span data-ttu-id="ada3a-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="ada3a-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="ada3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ada3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ada3a-103">Usuwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="ada3a-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="ada3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ada3a-104">SYNTAX</span></span>

### <span data-ttu-id="ada3a-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ada3a-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ada3a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ada3a-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ada3a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ada3a-107">DESCRIPTION</span></span>
<span data-ttu-id="ada3a-108">Usuwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="ada3a-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="ada3a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ada3a-109">EXAMPLES</span></span>

### <span data-ttu-id="ada3a-110">Przykład 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="ada3a-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="ada3a-111">Usuwa TestUbuntu. test. 1.0.0 z galerii stosów Azure.</span><span class="sxs-lookup"><span data-stu-id="ada3a-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="ada3a-112">Przykład 2: Remove-AzsGalleryItem za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="ada3a-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="ada3a-113">Usuwa TestUbuntu. test. 1.0.0 za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="ada3a-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="ada3a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ada3a-114">PARAMETERS</span></span>

### <span data-ttu-id="ada3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada3a-115">-DefaultProfile</span></span>
<span data-ttu-id="ada3a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ada3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada3a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ada3a-117">-InputObject</span></span>
<span data-ttu-id="ada3a-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ada3a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ada3a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ada3a-119">-Name</span></span>
<span data-ttu-id="ada3a-120">Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="ada3a-120">Identity of the gallery item.</span></span>
<span data-ttu-id="ada3a-121">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="ada3a-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="ada3a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ada3a-122">-PassThru</span></span>
<span data-ttu-id="ada3a-123">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ada3a-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ada3a-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ada3a-124">-SubscriptionId</span></span>
<span data-ttu-id="ada3a-125">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ada3a-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ada3a-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ada3a-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ada3a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ada3a-127">-Confirm</span></span>
<span data-ttu-id="ada3a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada3a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada3a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada3a-129">-WhatIf</span></span>
<span data-ttu-id="ada3a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ada3a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ada3a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ada3a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada3a-132">CommonParameters</span></span>
<span data-ttu-id="ada3a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada3a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ada3a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada3a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada3a-135">INPUTS</span></span>

### <span data-ttu-id="ada3a-136">Microsoft. Azure. PowerShell. polecenia cmdlet. Gallery. modele. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="ada3a-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="ada3a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ada3a-137">OUTPUTS</span></span>

### <span data-ttu-id="ada3a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ada3a-138">System.Boolean</span></span>



## <span data-ttu-id="ada3a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ada3a-139">NOTES</span></span>

<span data-ttu-id="ada3a-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ada3a-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ada3a-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ada3a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ada3a-142">INPUTobject <IGalleryIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ada3a-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ada3a-143">`[GalleryItemName <String>]`: Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="ada3a-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="ada3a-144">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="ada3a-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="ada3a-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ada3a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ada3a-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ada3a-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ada3a-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ada3a-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ada3a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada3a-148">RELATED LINKS</span></span>

