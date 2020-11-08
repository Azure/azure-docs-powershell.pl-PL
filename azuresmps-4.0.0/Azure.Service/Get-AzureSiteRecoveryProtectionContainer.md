---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054559"
---
# <span data-ttu-id="bdc62-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="bdc62-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="bdc62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdc62-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc62-103">Pobiera kontenery ochrony dla magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="bdc62-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="bdc62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdc62-104">SYNTAX</span></span>

### <span data-ttu-id="bdc62-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="bdc62-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bdc62-106">ById</span><span class="sxs-lookup"><span data-stu-id="bdc62-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bdc62-107">ByName</span><span class="sxs-lookup"><span data-stu-id="bdc62-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bdc62-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bdc62-108">DESCRIPTION</span></span>
<span data-ttu-id="bdc62-109">Polecenie cmdlet **Get-AzureSiteRecoveryProtectionContainer** pobiera kontenery ochrony dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bdc62-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="bdc62-110">Kontener ochrona jest logicznym kontenerem dla obiektów chronionych, takich jak maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="bdc62-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="bdc62-111">Zasady ochrony definiują ustawienia replikacji dla elementów chronionych i mogą być skojarzone z kontenerem ochrony i stosowane do jednostki chronionej.</span><span class="sxs-lookup"><span data-stu-id="bdc62-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="bdc62-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdc62-112">EXAMPLES</span></span>

### <span data-ttu-id="bdc62-113">Przykład 1: Pobierz chronione kontenery</span><span class="sxs-lookup"><span data-stu-id="bdc62-113">Example 1: Get protected containers</span></span>
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

<span data-ttu-id="bdc62-114">To polecenie uzyskuje chronione kontenery dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="bdc62-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="bdc62-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdc62-115">PARAMETERS</span></span>

### <span data-ttu-id="bdc62-116">-ID</span><span class="sxs-lookup"><span data-stu-id="bdc62-116">-Id</span></span>
<span data-ttu-id="bdc62-117">Określa identyfikator chronionego kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bdc62-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="bdc62-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdc62-118">-Name</span></span>
<span data-ttu-id="bdc62-119">Określa nazwę kontenera ochrony, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="bdc62-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="bdc62-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="bdc62-120">-Profile</span></span>
<span data-ttu-id="bdc62-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc62-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bdc62-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bdc62-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bdc62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc62-123">CommonParameters</span></span>
<span data-ttu-id="bdc62-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc62-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc62-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc62-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdc62-126">INPUTS</span></span>

## <span data-ttu-id="bdc62-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdc62-127">OUTPUTS</span></span>

## <span data-ttu-id="bdc62-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdc62-128">NOTES</span></span>

## <span data-ttu-id="bdc62-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdc62-129">RELATED LINKS</span></span>

[<span data-ttu-id="bdc62-130">Polecenia cmdlet usług Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="bdc62-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


