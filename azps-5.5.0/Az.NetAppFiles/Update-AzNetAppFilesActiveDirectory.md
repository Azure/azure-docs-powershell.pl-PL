---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203285"
---
# <span data-ttu-id="ae197-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ae197-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="ae197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae197-102">SYNOPSIS</span></span>
<span data-ttu-id="ae197-103">Aktualizuje konfigurację usługi Active Directory (ANF, Azure NetApp Files) na opcjonalne modyfikatory.</span><span class="sxs-lookup"><span data-stu-id="ae197-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="ae197-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae197-104">SYNTAX</span></span>

### <span data-ttu-id="ae197-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ae197-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae197-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae197-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae197-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae197-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae197-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae197-108">DESCRIPTION</span></span>
<span data-ttu-id="ae197-109">Polecenie **cmdlet Update-AzNetAppFilesAccount** modyfikuje konfigurację usługi Active Directory ANF.</span><span class="sxs-lookup"><span data-stu-id="ae197-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="ae197-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae197-110">EXAMPLES</span></span>

### <span data-ttu-id="ae197-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae197-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="ae197-112">To polecenie wykonuje aktualizację danej konfiguracji usługi Active Directory, modyfikując nazwę użytkownika na podaną nazwę użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ae197-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="ae197-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae197-113">PARAMETERS</span></span>

### <span data-ttu-id="ae197-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae197-114">-AccountName</span></span>
<span data-ttu-id="ae197-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="ae197-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ae197-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ae197-116">-AccountObject</span></span>
<span data-ttu-id="ae197-117">Konto obiektu usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="ae197-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="ae197-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="ae197-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="ae197-119">Identyfikator usługi Active Directory ANF</span><span class="sxs-lookup"><span data-stu-id="ae197-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae197-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="ae197-120">-AdName</span></span>
<span data-ttu-id="ae197-121">Nazwa komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ae197-121">Name of the active directory machine.</span></span>
<span data-ttu-id="ae197-122">Ten parametr opcjonalny jest używany tylko podczas tworzenia woluminu kerberos</span><span class="sxs-lookup"><span data-stu-id="ae197-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="ae197-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="ae197-123">-BackupOperator</span></span>
<span data-ttu-id="ae197-124">Użytkownicy, którzy mają zostać dodani do grupy active directory wbudowanego operatora kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ae197-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="ae197-125">Lista unikatowych nazw użytkowników bez specyfikatora domeny</span><span class="sxs-lookup"><span data-stu-id="ae197-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="ae197-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae197-126">-DefaultProfile</span></span>
<span data-ttu-id="ae197-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae197-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae197-128">— Dns</span><span class="sxs-lookup"><span data-stu-id="ae197-128">-Dns</span></span>
<span data-ttu-id="ae197-129">Rozdzielona przecinkami lista adresów IP serwera DNS (tylko IPv4) dla domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="ae197-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="ae197-130">— Domena</span><span class="sxs-lookup"><span data-stu-id="ae197-130">-Domain</span></span>
<span data-ttu-id="ae197-131">Nazwa domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="ae197-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="ae197-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae197-132">-InputObject</span></span>
<span data-ttu-id="ae197-133">Obiekt usługi Active Directory do usunięcia</span><span class="sxs-lookup"><span data-stu-id="ae197-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae197-134">- KdcIP</span><span class="sxs-lookup"><span data-stu-id="ae197-134">-KdcIP</span></span>
<span data-ttu-id="ae197-135">adresy IP serwera kdc dla komputera z usługą Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ae197-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="ae197-136">Ten parametr opcjonalny jest używany tylko podczas tworzenia woluminu kerberos.</span><span class="sxs-lookup"><span data-stu-id="ae197-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="ae197-137">- OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="ae197-137">-OrganizationalUnit</span></span>
<span data-ttu-id="ae197-138">Jednostka organizacyjna w usłudze Active Directory systemu Windows</span><span class="sxs-lookup"><span data-stu-id="ae197-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="ae197-139">— Hasło</span><span class="sxs-lookup"><span data-stu-id="ae197-139">-Password</span></span>
<span data-ttu-id="ae197-140">Hasło w formacie zwykłego tekstu administratora domeny usługi Active Directory, wartość jest maskowana w odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="ae197-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="ae197-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae197-141">-ResourceGroupName</span></span>
<span data-ttu-id="ae197-142">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="ae197-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ae197-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="ae197-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="ae197-144">Gdy protokół LDAP przez SSL/TLS jest włączony, klient LDAP musi mieć zakodowany certyfikat głównego urzędu certyfikacji usługi Active Directory z podpisem własnym, ten parametr opcjonalny jest używany tylko w przypadku dwóch protokołów z woluminami mapowania użytkowników LDAP.</span><span class="sxs-lookup"><span data-stu-id="ae197-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="ae197-145">— Witryna</span><span class="sxs-lookup"><span data-stu-id="ae197-145">-Site</span></span>
<span data-ttu-id="ae197-146">Witryna usługi Active Directory, do Kontroler domeny usługi odnajdowania</span><span class="sxs-lookup"><span data-stu-id="ae197-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="ae197-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="ae197-147">-SmbServerName</span></span>
<span data-ttu-id="ae197-148">Nazwa serwera SMB firmy NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="ae197-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="ae197-149">Ta nazwa zostanie zarejestrowana jako konto komputera w u góry usługi AD i będzie używana do instalacji woluminów</span><span class="sxs-lookup"><span data-stu-id="ae197-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="ae197-150">- Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="ae197-150">-Username</span></span>
<span data-ttu-id="ae197-151">Nazwa użytkownika administratora domeny usługi Active Directory</span><span class="sxs-lookup"><span data-stu-id="ae197-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="ae197-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae197-152">-Confirm</span></span>
<span data-ttu-id="ae197-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae197-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae197-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae197-154">-WhatIf</span></span>
<span data-ttu-id="ae197-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae197-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae197-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae197-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae197-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae197-157">CommonParameters</span></span>
<span data-ttu-id="ae197-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae197-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae197-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae197-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae197-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae197-160">INPUTS</span></span>

### <span data-ttu-id="ae197-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ae197-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ae197-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ae197-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="ae197-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae197-163">OUTPUTS</span></span>

### <span data-ttu-id="ae197-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ae197-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="ae197-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae197-165">NOTES</span></span>

## <span data-ttu-id="ae197-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae197-166">RELATED LINKS</span></span>
