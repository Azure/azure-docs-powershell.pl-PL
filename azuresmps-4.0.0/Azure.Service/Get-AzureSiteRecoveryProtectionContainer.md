---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405826"
---
# <span data-ttu-id="ec201-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ec201-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="ec201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec201-102">SYNOPSIS</span></span>
<span data-ttu-id="ec201-103">Pobiera kontenery ochrony dla magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="ec201-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="ec201-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec201-104">SYNTAX</span></span>

### <span data-ttu-id="ec201-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ec201-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec201-106">ById</span><span class="sxs-lookup"><span data-stu-id="ec201-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec201-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ec201-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec201-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec201-108">DESCRIPTION</span></span>
<span data-ttu-id="ec201-109">Polecenie **cmdlet Get-AzureSiteRecoveryProtectionContainer** pobiera kontenery ochrony dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ec201-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="ec201-110">Kontener ochrony to kontener logiczny dla chronionych obiektów, takich jak maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="ec201-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="ec201-111">Zasady ochrony definiują ustawienia replikacji elementów chronionych i mogą być skojarzone z kontenerem ochrony i stosowane do chronionej jednostki.</span><span class="sxs-lookup"><span data-stu-id="ec201-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="ec201-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec201-112">EXAMPLES</span></span>

### <span data-ttu-id="ec201-113">Przykład 1. Uzyskiwanie kontenerów chronionych</span><span class="sxs-lookup"><span data-stu-id="ec201-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="ec201-114">To polecenie pobiera kontenery chronione dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="ec201-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="ec201-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec201-115">PARAMETERS</span></span>

### <span data-ttu-id="ec201-116">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="ec201-116">-Id</span></span>
<span data-ttu-id="ec201-117">Określa identyfikator chronionego kontenera do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="ec201-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec201-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec201-118">-Name</span></span>
<span data-ttu-id="ec201-119">Określa nazwę kontenera ochrony do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="ec201-119">Specifies the name of a protection container to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec201-120">— Profil</span><span class="sxs-lookup"><span data-stu-id="ec201-120">-Profile</span></span>
<span data-ttu-id="ec201-121">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec201-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec201-122">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="ec201-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec201-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec201-123">CommonParameters</span></span>
<span data-ttu-id="ec201-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec201-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec201-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec201-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec201-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec201-126">INPUTS</span></span>

## <span data-ttu-id="ec201-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec201-127">OUTPUTS</span></span>

## <span data-ttu-id="ec201-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec201-128">NOTES</span></span>

## <span data-ttu-id="ec201-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec201-129">RELATED LINKS</span></span>




