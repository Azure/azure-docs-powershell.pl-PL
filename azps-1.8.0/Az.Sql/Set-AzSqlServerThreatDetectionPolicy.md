---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 8d58085aa55958e6e0fc9658d814d4bc05006fd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707713"
---
# <span data-ttu-id="5188d-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5188d-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="5188d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5188d-102">SYNOPSIS</span></span>
<span data-ttu-id="5188d-103">Ustawia zasady wykrywania zagrożeń na serwerze.</span><span class="sxs-lookup"><span data-stu-id="5188d-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="5188d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5188d-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5188d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5188d-105">DESCRIPTION</span></span>
<span data-ttu-id="5188d-106">Polecenie cmdlet **Set-AzSqlServerThreatDetectionPolicy** ustawia zasady wykrywania zagrożeń na platformie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5188d-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="5188d-107">W celu włączenia wykrywania zagrożeń na serwerze należy włączyć zasady inspekcji na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="5188d-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="5188d-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz nazwa_serwera identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="5188d-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="5188d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5188d-109">EXAMPLES</span></span>

### <span data-ttu-id="5188d-110">Przykład 1: Ustawianie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="5188d-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="5188d-111">To polecenie ustawia zasady wykrywania zagrożeń dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="5188d-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="5188d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5188d-112">PARAMETERS</span></span>

### <span data-ttu-id="5188d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5188d-113">-DefaultProfile</span></span>
<span data-ttu-id="5188d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5188d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5188d-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="5188d-115">-EmailAdmins</span></span>
<span data-ttu-id="5188d-116">Określa, czy zasady wykrywania zagrożeń kontaktują się z administratorami za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="5188d-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5188d-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="5188d-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="5188d-118">Określa tablicę typów wykrywania, które należy wykluczyć z zasad.</span><span class="sxs-lookup"><span data-stu-id="5188d-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="5188d-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5188d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5188d-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="5188d-120">Sql_Injection</span></span>
- <span data-ttu-id="5188d-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="5188d-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="5188d-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="5188d-122">Access_Anomaly</span></span>
- <span data-ttu-id="5188d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5188d-123">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5188d-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="5188d-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="5188d-125">Określa rozdzielaną średnikami listę adresów e-mail, do których zasady wysyłają powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="5188d-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5188d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5188d-126">-PassThru</span></span>
<span data-ttu-id="5188d-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5188d-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5188d-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5188d-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5188d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5188d-129">-ResourceGroupName</span></span>
<span data-ttu-id="5188d-130">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="5188d-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="5188d-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5188d-131">-RetentionInDays</span></span>
<span data-ttu-id="5188d-132">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="5188d-132">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5188d-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5188d-133">-ServerName</span></span>
<span data-ttu-id="5188d-134">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="5188d-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5188d-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5188d-135">-StorageAccountName</span></span>
<span data-ttu-id="5188d-136">Określa nazwę konta magazynu, które ma być używane.</span><span class="sxs-lookup"><span data-stu-id="5188d-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="5188d-137">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="5188d-137">Wildcards are not permitted.</span></span> <span data-ttu-id="5188d-138">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5188d-138">This parameter is not required.</span></span> <span data-ttu-id="5188d-139">Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zasad wykrywania zagrożeń w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="5188d-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="5188d-140">Jeśli zasada wykrywania tagu THEAD Database jest po raz pierwszy zdefiniowana, a ten parametr nie zostanie podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5188d-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5188d-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5188d-141">-Confirm</span></span>
<span data-ttu-id="5188d-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5188d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5188d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5188d-143">-WhatIf</span></span>
<span data-ttu-id="5188d-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5188d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5188d-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5188d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5188d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5188d-146">CommonParameters</span></span>
<span data-ttu-id="5188d-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5188d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5188d-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5188d-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5188d-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5188d-149">INPUTS</span></span>

### <span data-ttu-id="5188d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5188d-150">System.String</span></span>

### <span data-ttu-id="5188d-151">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5188d-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5188d-152">Microsoft. Azure. Commands. SQL. ThreatDetection. model. Detecttype []</span><span class="sxs-lookup"><span data-stu-id="5188d-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="5188d-153">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5188d-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5188d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5188d-154">OUTPUTS</span></span>

### <span data-ttu-id="5188d-155">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5188d-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="5188d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5188d-156">NOTES</span></span>

## <span data-ttu-id="5188d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5188d-157">RELATED LINKS</span></span>

[<span data-ttu-id="5188d-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5188d-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="5188d-159">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5188d-159">Remove-AzSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="5188d-160">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5188d-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
