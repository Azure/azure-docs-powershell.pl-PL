---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184858"
---
# <span data-ttu-id="dbab8-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="dbab8-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="dbab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbab8-102">SYNOPSIS</span></span>
<span data-ttu-id="dbab8-103">Tworzy nową konfigurację usługi Azure NetApp Files (ANF) w usłudze Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbab8-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="dbab8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dbab8-104">SYNTAX</span></span>

### <span data-ttu-id="dbab8-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dbab8-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbab8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbab8-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbab8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dbab8-107">DESCRIPTION</span></span>
<span data-ttu-id="dbab8-108">Polecenie **cmdlet New-AzNetAppFilesActiveDirectory** tworzy nową konfigurację usługi Active Directory dla konta ANF.</span><span class="sxs-lookup"><span data-stu-id="dbab8-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="dbab8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dbab8-109">EXAMPLES</span></span>

### <span data-ttu-id="dbab8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dbab8-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="dbab8-111">To polecenie pobiera hasło usługi AD z programu Promt do nowej konfiguracji usługi Active Directory dla konta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="dbab8-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="dbab8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbab8-112">PARAMETERS</span></span>

### <span data-ttu-id="dbab8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbab8-113">-AccountName</span></span>
<span data-ttu-id="dbab8-114">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="dbab8-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbab8-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="dbab8-115">-AccountObject</span></span>
<span data-ttu-id="dbab8-116">Konto dla nowego obiektu zasad kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="dbab8-116">The Account for the new Backup Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbab8-117">—AdName</span><span class="sxs-lookup"><span data-stu-id="dbab8-117">-AdName</span></span>
<span data-ttu-id="dbab8-118">Nazwa komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbab8-118">Name of the active directory machine.</span></span>
<span data-ttu-id="dbab8-119">Ten parametr opcjonalny jest używany tylko podczas tworzenia woluminu kerberos</span><span class="sxs-lookup"><span data-stu-id="dbab8-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="dbab8-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="dbab8-120">-BackupOperator</span></span>
<span data-ttu-id="dbab8-121">Użytkownicy, którzy mają zostać dodani do grupy active directory wbudowanego operatora kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="dbab8-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="dbab8-122">Lista unikatowych nazw użytkowników bez specyfikatora domeny</span><span class="sxs-lookup"><span data-stu-id="dbab8-122">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbab8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbab8-123">-DefaultProfile</span></span>
<span data-ttu-id="dbab8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbab8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbab8-125">— Dns</span><span class="sxs-lookup"><span data-stu-id="dbab8-125">-Dns</span></span>
<span data-ttu-id="dbab8-126">Rozdzielona przecinkami lista adresów IP serwera DNS (tylko IPv4) dla domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="dbab8-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbab8-127">— Domena</span><span class="sxs-lookup"><span data-stu-id="dbab8-127">-Domain</span></span>
<span data-ttu-id="dbab8-128">Nazwa domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="dbab8-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="dbab8-129">- KdcIP</span><span class="sxs-lookup"><span data-stu-id="dbab8-129">-KdcIP</span></span>
<span data-ttu-id="dbab8-130">adresy IP serwera kdc dla komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbab8-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="dbab8-131">Ten parametr opcjonalny jest używany tylko podczas tworzenia woluminu kerberos.</span><span class="sxs-lookup"><span data-stu-id="dbab8-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="dbab8-132">- OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="dbab8-132">-OrganizationalUnit</span></span>
<span data-ttu-id="dbab8-133">Jednostka organizacyjna w usłudze Active Directory systemu Windows</span><span class="sxs-lookup"><span data-stu-id="dbab8-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="dbab8-134">— Hasło</span><span class="sxs-lookup"><span data-stu-id="dbab8-134">-Password</span></span>
<span data-ttu-id="dbab8-135">Hasło w formacie zwykłego tekstu administratora domeny usługi Active Directory, wartość jest maskowana w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="dbab8-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbab8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbab8-136">-ResourceGroupName</span></span>
<span data-ttu-id="dbab8-137">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="dbab8-137">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbab8-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="dbab8-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="dbab8-139">Gdy protokół LDAP przez SSL/TLS jest włączony, klient LDAP musi mieć zakodowany certyfikat głównego urzędu certyfikacji usługi Active Directory z podpisem własnym, ten parametr opcjonalny jest używany tylko w przypadku dwóch protokołów z woluminami mapowania użytkowników LDAP.</span><span class="sxs-lookup"><span data-stu-id="dbab8-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="dbab8-140">— Witryna</span><span class="sxs-lookup"><span data-stu-id="dbab8-140">-Site</span></span>
<span data-ttu-id="dbab8-141">Witryna usługi Active Directory, do Kontroler domeny usługi odnajdowania</span><span class="sxs-lookup"><span data-stu-id="dbab8-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="dbab8-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="dbab8-142">-SmbServerName</span></span>
<span data-ttu-id="dbab8-143">Nazwa serwera SMB systemu NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="dbab8-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="dbab8-144">Ta nazwa zostanie zarejestrowana jako konto komputera w u góry usługi AD i będzie używana do instalacji woluminów</span><span class="sxs-lookup"><span data-stu-id="dbab8-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="dbab8-145">- Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="dbab8-145">-Username</span></span>
<span data-ttu-id="dbab8-146">Nazwa użytkownika administratora domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="dbab8-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="dbab8-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbab8-147">-Confirm</span></span>
<span data-ttu-id="dbab8-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dbab8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbab8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbab8-149">-WhatIf</span></span>
<span data-ttu-id="dbab8-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbab8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbab8-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dbab8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbab8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbab8-152">CommonParameters</span></span>
<span data-ttu-id="dbab8-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbab8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbab8-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbab8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbab8-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbab8-155">INPUTS</span></span>

### <span data-ttu-id="dbab8-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="dbab8-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="dbab8-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbab8-157">OUTPUTS</span></span>

### <span data-ttu-id="dbab8-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="dbab8-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="dbab8-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dbab8-159">NOTES</span></span>

## <span data-ttu-id="dbab8-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbab8-160">RELATED LINKS</span></span>
