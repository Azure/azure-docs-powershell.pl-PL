---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055773"
---
# <span data-ttu-id="18306-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="18306-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="18306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18306-102">SYNOPSIS</span></span>
<span data-ttu-id="18306-103">Umożliwia przekazanie elementu galerii dostawców do magazynu.</span><span class="sxs-lookup"><span data-stu-id="18306-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="18306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18306-104">SYNTAX</span></span>

### <span data-ttu-id="18306-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="18306-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18306-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="18306-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18306-107">Opis</span><span class="sxs-lookup"><span data-stu-id="18306-107">DESCRIPTION</span></span>
<span data-ttu-id="18306-108">Umożliwia przekazanie elementu galerii dostawców do magazynu.</span><span class="sxs-lookup"><span data-stu-id="18306-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="18306-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18306-109">EXAMPLES</span></span>

### <span data-ttu-id="18306-110">Przykład 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="18306-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="18306-111">Przekazanie TestUbuntu. test. 1.0.0 do galerii.</span><span class="sxs-lookup"><span data-stu-id="18306-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="18306-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18306-112">PARAMETERS</span></span>

### <span data-ttu-id="18306-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18306-113">-DefaultProfile</span></span>
<span data-ttu-id="18306-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18306-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18306-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="18306-115">-GalleryItemUri</span></span>
<span data-ttu-id="18306-116">Identyfikator URI dla pakietu galerii, który został już przekazany w trybie online.</span><span class="sxs-lookup"><span data-stu-id="18306-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18306-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="18306-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="18306-118">Lokalizacja ładunku elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="18306-118">Location of gallery item payload.</span></span>
<span data-ttu-id="18306-119">Aby skonstruować, zobacz sekcję notatki dla właściwości GALLERYITEMURIPAYLOAD i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="18306-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="18306-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="18306-120">-SubscriptionId</span></span>
<span data-ttu-id="18306-121">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18306-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18306-122">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="18306-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18306-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18306-123">-Confirm</span></span>
<span data-ttu-id="18306-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18306-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18306-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18306-125">-WhatIf</span></span>
<span data-ttu-id="18306-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18306-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18306-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18306-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18306-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18306-128">CommonParameters</span></span>
<span data-ttu-id="18306-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18306-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18306-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18306-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18306-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18306-131">INPUTS</span></span>

### <span data-ttu-id="18306-132">Microsoft. Azure. PowerShell. polecenia cmdlet. Gallery. models. Api20150401. IGalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="18306-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="18306-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18306-133">OUTPUTS</span></span>

### <span data-ttu-id="18306-134">Microsoft. Azure. PowerShell. polecenia cmdlet. Gallery. models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="18306-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="18306-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18306-135">NOTES</span></span>

<span data-ttu-id="18306-136">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="18306-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18306-137">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18306-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="18306-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : Lokalizacja ładunku elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="18306-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="18306-139">`[GalleryItemUri <String>]`: Identyfikator URI pakietu galerii, który został już przekazany w trybie online.</span><span class="sxs-lookup"><span data-stu-id="18306-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="18306-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18306-140">RELATED LINKS</span></span>

