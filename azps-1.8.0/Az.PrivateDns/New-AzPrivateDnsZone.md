---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 20922936f754f18d2ee26631dc616d9723cdc5e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708748"
---
# <span data-ttu-id="29330-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="29330-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="29330-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29330-102">SYNOPSIS</span></span>
<span data-ttu-id="29330-103">Tworzy nową prywatną strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="29330-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="29330-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29330-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29330-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29330-105">DESCRIPTION</span></span>
<span data-ttu-id="29330-106">Polecenie cmdlet **New-AzPrivateDnsZone** tworzy nową strefę DNS (Private Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="29330-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="29330-107">Musisz określić unikatową nazwę prywatnej strefy DNS dla parametru *name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="29330-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="29330-108">Po utworzeniu strefy Użyj polecenia cmdlet New-AzPrivateDnsRecordSet, aby utworzyć zestaw rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="29330-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="29330-109">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="29330-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="29330-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29330-110">EXAMPLES</span></span>

### <span data-ttu-id="29330-111">Przykład 1. Tworzenie prywatnej strefy DNS</span><span class="sxs-lookup"><span data-stu-id="29330-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="29330-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29330-112">PARAMETERS</span></span>

### <span data-ttu-id="29330-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29330-113">-DefaultProfile</span></span>
<span data-ttu-id="29330-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29330-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29330-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29330-115">-Name</span></span>
<span data-ttu-id="29330-116">Określa nazwę prywatnej strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="29330-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="29330-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29330-117">-ResourceGroupName</span></span>
<span data-ttu-id="29330-118">Określa grupę zasobów, w której ma zostać utworzona strefa.</span><span class="sxs-lookup"><span data-stu-id="29330-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="29330-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="29330-119">-Tag</span></span>
<span data-ttu-id="29330-120">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="29330-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="29330-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29330-121">-Confirm</span></span>
<span data-ttu-id="29330-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29330-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29330-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29330-123">-WhatIf</span></span>
<span data-ttu-id="29330-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29330-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29330-125">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29330-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29330-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29330-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29330-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29330-127">CommonParameters</span></span>
<span data-ttu-id="29330-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29330-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29330-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29330-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29330-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29330-130">INPUTS</span></span>

### <span data-ttu-id="29330-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="29330-131">None</span></span>

## <span data-ttu-id="29330-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29330-132">OUTPUTS</span></span>

### <span data-ttu-id="29330-133">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="29330-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="29330-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29330-134">NOTES</span></span>

## <span data-ttu-id="29330-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29330-135">RELATED LINKS</span></span>

[<span data-ttu-id="29330-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="29330-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="29330-137">Nowe — AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="29330-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="29330-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="29330-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)