---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: cde8f48ebef73e3669a82f05c2ba91a4a4e4c582
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973489"
---
# <span data-ttu-id="9da77-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="9da77-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="9da77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9da77-102">SYNOPSIS</span></span>
<span data-ttu-id="9da77-103">Failovers an Azure SQL Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="9da77-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="9da77-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9da77-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9da77-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9da77-105">DESCRIPTION</span></span>
<span data-ttu-id="9da77-106">Polecenie cmdlet **Invoke-AzSqlInstanceFailover trybu failovers** wystąpienia zarządzanego języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9da77-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="9da77-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9da77-107">EXAMPLES</span></span>

### <span data-ttu-id="9da77-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9da77-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="9da77-109">To polecenie będzie trybu failover podstawowej repliki wystąpienia o nazwie "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="9da77-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="9da77-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9da77-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="9da77-111">To polecenie będzie trybu failover czytelnej repliki pomocniczej zarządzanego wystąpienia "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="9da77-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="9da77-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9da77-112">PARAMETERS</span></span>

### <span data-ttu-id="9da77-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9da77-113">-AsJob</span></span>
<span data-ttu-id="9da77-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9da77-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9da77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da77-115">-DefaultProfile</span></span>
<span data-ttu-id="9da77-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9da77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da77-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9da77-117">-Force</span></span>
<span data-ttu-id="9da77-118">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="9da77-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9da77-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9da77-119">-Name</span></span>
<span data-ttu-id="9da77-120">Nazwa wystąpienia języka Azure SQL do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9da77-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da77-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9da77-121">-PassThru</span></span>
<span data-ttu-id="9da77-122">Po pomyślnym wykonaniu zwraca wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="9da77-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="9da77-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9da77-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9da77-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="9da77-124">-ReadableSecondary</span></span>
<span data-ttu-id="9da77-125">Failover the readable secondary replica instead of the default primary replica</span><span class="sxs-lookup"><span data-stu-id="9da77-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="9da77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da77-126">-ResourceGroupName</span></span>
<span data-ttu-id="9da77-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9da77-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da77-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9da77-128">-Confirm</span></span>
<span data-ttu-id="9da77-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9da77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da77-130">-WhatIf</span></span>
<span data-ttu-id="9da77-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da77-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9da77-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9da77-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da77-133">CommonParameters</span></span>
<span data-ttu-id="9da77-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da77-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9da77-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da77-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9da77-136">INPUTS</span></span>

### <span data-ttu-id="9da77-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9da77-137">System.String</span></span>

## <span data-ttu-id="9da77-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9da77-138">OUTPUTS</span></span>

## <span data-ttu-id="9da77-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9da77-139">NOTES</span></span>

## <span data-ttu-id="9da77-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9da77-140">RELATED LINKS</span></span>
