---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: d135cc72a9830535d6b67ce80f29725a569894e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977786"
---
# <span data-ttu-id="4599a-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4599a-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="4599a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4599a-102">SYNOPSIS</span></span>
<span data-ttu-id="4599a-103">Tworzy nową prywatną strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="4599a-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="4599a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4599a-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4599a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4599a-105">DESCRIPTION</span></span>
<span data-ttu-id="4599a-106">Polecenie **cmdlet New-AzPrivateDnsZone** tworzy nową strefę DNS (Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4599a-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="4599a-107">Musisz określić unikatową nazwę prywatnej strefy DNS dla *parametru Name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="4599a-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="4599a-108">Po utworzeniu strefy użyj polecenia cmdlet New-AzPrivateDnsRecordSet, aby utworzyć zestawy rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="4599a-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="4599a-109">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4599a-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="4599a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4599a-110">EXAMPLES</span></span>

### <span data-ttu-id="4599a-111">Przykład 1. Tworzenie prywatnej strefy DNS</span><span class="sxs-lookup"><span data-stu-id="4599a-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="4599a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4599a-112">PARAMETERS</span></span>

### <span data-ttu-id="4599a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4599a-113">-DefaultProfile</span></span>
<span data-ttu-id="4599a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4599a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4599a-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4599a-115">-Name</span></span>
<span data-ttu-id="4599a-116">Określa nazwę prywatnej strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4599a-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="4599a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4599a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4599a-118">Określa grupę zasobów, w której ma być tworzyć strefę.</span><span class="sxs-lookup"><span data-stu-id="4599a-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="4599a-119">— Tag</span><span class="sxs-lookup"><span data-stu-id="4599a-119">-Tag</span></span>
<span data-ttu-id="4599a-120">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="4599a-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4599a-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4599a-121">-Confirm</span></span>
<span data-ttu-id="4599a-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4599a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4599a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4599a-123">-WhatIf</span></span>
<span data-ttu-id="4599a-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4599a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4599a-125">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4599a-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4599a-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4599a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4599a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4599a-127">CommonParameters</span></span>
<span data-ttu-id="4599a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4599a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4599a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4599a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4599a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4599a-130">INPUTS</span></span>

### <span data-ttu-id="4599a-131">Brak</span><span class="sxs-lookup"><span data-stu-id="4599a-131">None</span></span>

## <span data-ttu-id="4599a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4599a-132">OUTPUTS</span></span>

### <span data-ttu-id="4599a-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4599a-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="4599a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4599a-134">NOTES</span></span>

## <span data-ttu-id="4599a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4599a-135">RELATED LINKS</span></span>

[<span data-ttu-id="4599a-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4599a-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="4599a-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4599a-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="4599a-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4599a-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
