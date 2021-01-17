---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385772"
---
# <span data-ttu-id="b5844-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="b5844-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="b5844-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5844-102">SYNOPSIS</span></span>
<span data-ttu-id="b5844-103">Umożliwia utworzenie obiektu w celu zaktualizowania właściwości karty sieciowej serwera replikacji.</span><span class="sxs-lookup"><span data-stu-id="b5844-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="b5844-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5844-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5844-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5844-105">DESCRIPTION</span></span>
<span data-ttu-id="b5844-106">Polecenie cmdlet New-AzMigrateNicMapping tworzy mapowanie źródłowej karty sieciowej podłączonej do serwera, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="b5844-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="b5844-107">Ten obiekt jest dostarczany jako wejście do polecenia cmdlet Set-AzMigrateServerReplication w celu zaktualizowania karty NIC i jej właściwości dla serwera replikowanego.</span><span class="sxs-lookup"><span data-stu-id="b5844-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="b5844-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5844-108">EXAMPLES</span></span>

### <span data-ttu-id="b5844-109">Przykład 1. Tworzenie obiektu karty interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="b5844-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="b5844-110">Tworzy obiekt aktualizacji karty sieciowej.</span><span class="sxs-lookup"><span data-stu-id="b5844-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="b5844-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5844-111">PARAMETERS</span></span>

### <span data-ttu-id="b5844-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="b5844-112">-NicID</span></span>
<span data-ttu-id="b5844-113">Określa identyfikator karty sieciowej, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="b5844-113">Specifies the ID of the NIC to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5844-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="b5844-114">-TargetNicIP</span></span>
<span data-ttu-id="b5844-115">Określa adres IP w podsieci docelowej, który ma być wykorzystywany przez kartę NIC.</span><span class="sxs-lookup"><span data-stu-id="b5844-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5844-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="b5844-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="b5844-117">Określa, czy karta sieciowa do zaktualizowania będzie podstawowa, pomocnicza, czy nie.</span><span class="sxs-lookup"><span data-stu-id="b5844-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5844-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="b5844-118">-TargetNicSubnet</span></span>
<span data-ttu-id="b5844-119">Określa nazwę podsieci dla karty sieciowej w docelowej sieci wirtualnej, do której należy przeprowadzić migrację serwera.</span><span class="sxs-lookup"><span data-stu-id="b5844-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5844-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5844-120">CommonParameters</span></span>
<span data-ttu-id="b5844-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5844-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5844-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5844-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5844-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5844-123">INPUTS</span></span>

## <span data-ttu-id="b5844-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5844-124">OUTPUTS</span></span>

### <span data-ttu-id="b5844-125">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="b5844-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="b5844-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5844-126">NOTES</span></span>

<span data-ttu-id="b5844-127">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b5844-127">ALIASES</span></span>

## <span data-ttu-id="b5844-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5844-128">RELATED LINKS</span></span>

